# nook
https://github.com/nook
import csv
import pandas as pd 
import os
import math
data = pd.read_csv('internal_all - internal_all.csv')
data = data[['Address', 'H1-1', 'текст 1']]
# data = data[~data['Address'].str.contains('page')]
# data = data.drop(index=0)
rows_in_rss = 1000 # количество строк в одном rss-канале
total_rows = len(data) - 1
total_xml_file = math.ceil((total_rows-1)/rows_in_rss)
print('Всего в файле строк:', total_rows)
print('Будет сгенерировано xml-файлов:', total_xml_file)
