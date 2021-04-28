每个记录由三个属性组成：
is_sarcastic：讽刺型标题：1；否则：0
headline：新闻文章的标题
article_link：链接到原始新闻文章。可用于收集补充数据

以下代码用于读取数据：
import json

def parse_data(file):
    for l in open(file,'r'):
        yield json.loads(l)

data = list(parse_data('./Sarcasm_Headlines_Dataset.json'))