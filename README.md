0604 14주_자연어처리

2017 passage self matching 등장

cnn은 위치 정보가 없어서 rnn으로 쪼개기도 한다..
oove일 수도 았으니 lstm넣어서 

임베딩 값을 양방향 lstm에 넣어서 정방향, 역방향 context를 합쳐서 만든다

co-attention은 질문과 context 사이의 attention score

leads는 president에 걸린다.

h1과 query와의 각 단어와의 내적을 계산해서 softmax
그러한 것들이 t개 ( context2query)

softmax를 하지 않고  hn에서 가장 큰 값 하나씩 모아서 softmax -> 1개의 값 도출

attention 2개와 원래의 임베딩값 

질문과 답 사이의 후보를 찾는 것이 co-attention

self-attention은 후보들 중에 고민해서 고르는 것

attention 값이 t개씩

1 0 0 0 0 0
0 0 1 0 0 0

start의 결과를 다시 lstm으로 end로 보낸다.

BiDAF:
일부가 겹쳤을 때 precision과 recall 
precision : 분모는 내가 내뱉은 것 / 
recall: 분모가 정답 / 분자는 맞힌 수

fi-score는 2pr/p+r

encoding , co-attention

Bert
triviaQA로 추가학습한 결과

결국 언어모델의 다음 답을 맞히는 것에 가까워짐
