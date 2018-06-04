---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IInkRecognizerContext::get_SuffixText


## -description



Gets or sets the characters that come after the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection in the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object.



This property is read/write.


## -parameters


## -remarks



The suffix helps improve recognition results by supplying the recognizer with more context about the handwriting.

Setting the <b>SuffixText</b> property succeeds only if the <a href="https://msdn.microsoft.com/af31559b-741e-4af2-8c35-9e34ad1af85f">Strokes</a> property is <b>NULL</b>. You must set the <b>SuffixText</b> property before you attach an <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection to the <b>Strokes</b> property of the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a>, or you must set the <b>Strokes</b> property to <b>NULL</b> and then set the <b>SuffixText</b> property.

<div class="alert"><b>Note</b>  If you use the latter method, you may need to reattach the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection to the <a href="https://msdn.microsoft.com/af31559b-741e-4af2-8c35-9e34ad1af85f">Strokes</a> property of the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object.</div>
<div> </div>
Setting the <b>SuffixText</b> property to <b>NULL</b> removes any suffix text from the recognizer context.

The suffix text is ignored unless you have set both the <a href="https://msdn.microsoft.com/ab9f4164-ea07-41d1-be6a-50009fa9464d">Coerce</a> and <b>WordMode</b><b>InkRecognitionModes</b> flags in the <a href="https://msdn.microsoft.com/71b02f99-4076-4c56-b88a-4201b7033411">RecognitionFlags</a> property.

The <a href="https://msdn.microsoft.com/fe5c91ce-c53e-4f33-bd67-2f1c10e5cf97">PrefixText</a> property gets or sets the characters that come before the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection in the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object and also helps improve the recognition result.

If your application provides a correction interface when converting ink to text, the application may allow the user to select characters within a word and use the stylus to generate replacement characters. Your application can use the <a href="https://msdn.microsoft.com/fe5c91ce-c53e-4f33-bd67-2f1c10e5cf97">PrefixText</a> and <b>SuffixText</b> properties to improve recognition of the new ink.




## -see-also




<a href="tablet.iinkrecognizercontext">IInkRecognizerContext</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>



<a href="https://msdn.microsoft.com/fe5c91ce-c53e-4f33-bd67-2f1c10e5cf97">PrefixText Property</a>



<a href="https://msdn.microsoft.com/71b02f99-4076-4c56-b88a-4201b7033411">RecognitionFlags Property</a>



<a href="https://msdn.microsoft.com/b65f1b71-b0a4-4de2-9321-f660bcd2d3ce">Strokes Property</a>
 

 

