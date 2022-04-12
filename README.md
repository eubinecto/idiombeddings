# Idiombeddings - a consituent-induced embeddings for idioms


## The Rationale

I think we could improve machines in processing idioms if we draw inspirations from how humans go about learning idioms. That is, if we could introduce human-inspired inductived biases to language models, we may be able to improve their performance on figurative processing.


<img width="795" alt="image" src="https://user-images.githubusercontent.com/56193069/163037939-e15cdfed-0afb-4842-ab39-6f03eaac2ddd.png">


But first, why do we even need to have machines better understand idioms?  It is because, although a huge progress has been made within Natural Language Processing (NLP) in recent years, figurative processing has always been a “pain in the neck” in NLP, so to speak. Take BERT as an example. It is a connectionists language model that can be finetuned to fill-in-the-blanks (top left), answer a question (top right), summarize a pargraph (bottom left), analyse sentiments (bottom right), etc. These are by no means easy tasks to machines, but as you can see from the examples above, the performance of BERT on these colloquial tasks are quite impressive. 


<img width="807" alt="image" src="https://user-images.githubusercontent.com/56193069/163038008-49cbe6ca-4c1e-4a23-8c84-0defcc2f0e49.png">

However, when it comes to processing idioms, BERT is far from impressive. Without even getting into the literature, you can already see how replacing get ready (left) to wet my gills (right) substantially changes the predictions on fill-in-the-blanks task, although the two phrases essentially mean the same thing. Ideally, the probability distribution should stay more or less the same, but it doesn’t. This is because, as with many other language models, BERT falls short at processing the figures of speech.

<img width="791" alt="image" src="https://user-images.githubusercontent.com/56193069/163038079-e791691a-c46c-4356-aa6f-79eb6541f7a2.png">

Given that the goal of NLP is to “process all forms of natural language well” (Haagsma, 2020),  NLP researchers unanimously started to point out this problem in recent years. Just like how humans process natural language, a well-designed NLP unit should be able to process any forms of natural languge, whether it be formal (e.g. writing an email), colloquial (e.g. chatting with friends), canonical / structured (e.g. writing essays). While some success has been made in processing canonical language as we saw above, language models are “still far from revealing implicit meaning” of the figures of speech (Shawartz &  Dagan, 2019). Likewise, “Idiomatic meaning gets overpowered by compositional meaning of the expressions” ( Saxemna & Paul, 2020), partly because their constituents are more often found separately in many corpora than together as idioms. All in all, “figurative language is an important research area for computational & congnitive linguistics”, as ACL remarks in their report on 2020 workshop, which was aptly named, Figurative Language Processing. 

<img width="443" alt="image" src="https://user-images.githubusercontent.com/56193069/163038153-363a4bcc-d4ff-4101-b923-1ab0243cef71.png">


So, there is a huge room for improvement in figurative language processing, but where do we get the ideas for the improvement? We could take various approaches to this, but Shawatz & Dagan suggest (2019) what I think is arguably the most sensible approach:  “get some inspiration from the way that humans learn idioms”.  We at least have a working answer in the human brain, however elusive it may be, so it is sensible to at least try to replicate this  in machines rather than to invent a completely new solution from scratch. It works in the human brain, so  it may as well work in connectionsists language models ( layers of artifical neural networks).  And this, this is what I mean by SLA could suggest better biases to NLP. That is, we could improve the performance of such language models on processing idioms, specifically BERT for my dissertation, by drawing inspirations (i.e. biases) from how humans learn idioms.   

<img width="621" alt="image" src="https://user-images.githubusercontent.com/56193069/163038193-eb63ddc2-04af-4ce4-a6e7-ddce3503d952.png">

So, there is a huge room for improvement in figurative language processing, but where do we get the ideas for the improvement? We could take various approaches to this, but Shawatz & Dagan suggest (2019) what I think is arguably the most sensible approach:  “get some inspiration from the way that humans learn idioms”.  We at least have a working answer in the human brain, however elusive it may be, so it is sensible to at least try to replicate this  in machines rather than to invent a completely new solution from scratch. It works in the human brain, so  it may as well work in connectionsists language models ( layers of artifical neural networks).  And this, this is what I mean by SLA could suggest better biases to NLP. That is, we could improve the performance of such language models on processing idioms, specifically BERT for my dissertation, by drawing inspirations (i.e. biases) from how humans learn idioms.   

What better biases have I found, then?  the Global Elaboration Hypothesis  posits (Levorato & Cacciari, 1995; karlson, 2019) that both L1 and L2 learners may start  learning idioms by first deducing the figurative meaning from the literal meaning, for those idioms that are yet to take place in their mental lexicon (vocabulary). It is not like they get the metaphor behing the literal interpretation right off the bat. However, as the learners age and contine learing those idioms, they gradually treat idioms as a single chunk and stop relying on analogies to get the figurative meaning. For example, when L2 learners of English encounter the idiom *throw the baby out with the bathwater* for the first time, their first reaction is to interpret the meaning literally, which they analogize with a given context to guess the figurative meaning, *to ignore potentially important things.* However, as they go along, the gradually stop imagining babies being thrown altogether with dirty water in their minds, and at the end, they don’t even think of babies when using *throw baby out with the bathwater* in its idioamtic sense - they  just use it as a single chunk at the end of their learning.

If that’s how we go about learning idioms, that is, if humans use the literal interpretaion of idioms to “bootstrap” their understaning on the figurative meaning, so to speak, then there is nothing stopping us to expect that the bootstrapping bias as such may be useful for teaching idioms to language models.
