# Regular-Expression_study
정규 표현식(RegExp)에 대한 설명과 예제를 통한 학습.
<hr>
<h3>💡정규 표현식이란? </h3>
  정규 표현식(Regular Expression, RegExp)은 문자열에서 특정한 규칙(패턴)을 갖는 문자열을 찾거나, 대체하거나, 추출하는 데 사용되는 문자열 패턴의 표현 방법입니다.

<h3> 특징 </h3>
- 일반적으로 텍스트 검색과 문자열 처리에 사용되며, 다양한 프로그래밍 언어에서 지원됩니다.
- 특정한 패턴을 나타내는 문자열을 일괄적으로 처리하거나, 특정한 패턴에 대한 검색 또는 추출을 쉽게 수행할 수 있습니다.

<h3> 문자 </h3>
정규 표현식에서는 다양한 문자를 조합하여 표현할 수 있습니다.<br>
<b>1. 일반문자</b><br>
a, b, c, ..., z, A, B, C, ..., Z: 알파벳 소문자와 대문자<br>
0, 1, 2, ..., 9: 숫자<br>
_, -, ., +, 등: 기호<br>
<br>

<b>2. 메타문자</b><br>
. (점): 어떤 문자 하나와 일치합니다.<br>
(별표): 앞에 있는 문자가 0번 이상 반복되는 문자열과 일치합니다.<br>
(플러스): 앞에 있는 문자가 1번 이상 반복되는 문자열과 일치합니다.<br>
? (물음표): 앞에 있는 문자가 0번 또는 1번 나타나는 문자열과 일치합니다.<br>
| (파이프): 대안을 나타냅니다. A|B는 A 또는 B와 일치합니다.<br>
() (괄호): 그룹을 지정합니다. (ABC)는 ABC와 일치합니다.<br>
[] (대괄호): 문자 클래스를 나타냅니다. [abc]는 a, b, c 중 하나와 일치합니다.<br>
{} (중괄호): 반복을 나타냅니다. A{2}는 A가 2번 반복되는 문자열과 일치합니다.<br>

<b>3. 특수문자(이스케이프)</b> <br>
\d: 숫자와 일치합니다.<br>
\D: 숫자가 아닌 문자와 일치합니다.<br>
\w: 알파벳 소문자, 대문자, 숫자와 일치합니다.<br>
\W: 알파벳 소문자, 대문자, 숫자가 아닌 문자와 일치합니다.<br>
\s: 공백 문자와 일치합니다.<br>
\S: 공백 문자가 아닌 문자와 일치합니다.<br>
<br>
  
<h3> 정규 표현식 함수 </h3>
re.search(pattern, string)
문자열(string)에서 정규 표현식(pattern)과 일치하는 첫 번째 부분을 찾아서 MatchObject 객체를 





<code>
import re

# 문자열에서 패턴 찾기
pattern = r'apple'
text = 'I like apple.'
result = re.search(pattern, text)
if result:
    print('찾은 패턴:', result.group())
else:
    print('일치하는 패턴이 없습니다.')

# 문자열에서 모든 패턴 찾기
pattern = r'apple'
text = 'I like apple. I have an apple.'
results = re.findall(pattern, text)
if results:
    print('찾은 패턴:', results)
else:
    print('일치하는 패턴이 없습니다.')

# 패턴으로 문자열 대체하기
pattern = r'apple'
replace = 'orange'
text = 'I like apple. I have an apple.'
result = re.sub(pattern, replace, text)
print('바뀐 문자열:', result)

# 패턴으로 문자열 분리하기
pattern = r'\s+'
text = 'I like apple. I have an apple.'
results = re.split(pattern, text)
print('분리된 문자열:', results)
  </code>


