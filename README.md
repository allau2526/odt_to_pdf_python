# odt_to_pdf_python
Надо преобразовать odt в pdf используя Python скрипт
import pypandoc
import os

os.environ.setdefault('PYPANDOC_PANDOC', 'C:\\Users\\User\\AppData\\Local\\Pandoc\\pandoc.exe')
file_path = "testo4.odt"
output1 = pypandoc.convert_file(file_path, 'pdf', outputfile= 'test.pdf',
                extra_args = ['--pdf-engine=xelatex' ,'-V', 'geometry:margin=1.5cm', '-V','mainfont="Arial"',])
                
                
у меня такой код, проблема заключаается в том что не выходят таблицы
