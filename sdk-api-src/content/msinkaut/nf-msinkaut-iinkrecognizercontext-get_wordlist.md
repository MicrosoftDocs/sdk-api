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

# IInkRecognizerContext::get_WordList


## -description



Gets or sets the word list that is used in the recognition process to improve the recognition results.



This property is read/write.


## -parameters


## -remarks



Setting this property succeeds only if the <a href="https://msdn.microsoft.com/b65f1b71-b0a4-4de2-9321-f660bcd2d3ce">Strokes</a> property is <b>NULL</b>. You must set the <b>WordList</b> property before you attach an <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection to the <b>Strokes</b> property of the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> or you must set the <b>Strokes</b> property to <b>NULL</b> and then set the <b>WordList</b> property (and possibly reattach the InkStrokes collection).

To remove the current word list and use the user dictionary, set this property to <b>NULL</b>. Any subsequent modification of the <a href="https://msdn.microsoft.com/d189fd13-ec69-45dc-8be4-fea48f337636">InkWordList</a> object does not modify the recognition outcome. If you want to change the word list, first set this property to <b>NULL</b>, modify the InkWordList, and then re-attach it to the InkRecognizerContext by assigning it to the <b>WordList</b> property.

Use the <a href="https://msdn.microsoft.com/11a76706-e2e5-4ae5-bdc2-5354514ea29f">Factoid</a> property to limit the search to the word list that is associated with the context. You may also need to set the <a href="https://msdn.microsoft.com/71b02f99-4076-4c56-b88a-4201b7033411">RecognitionFlags</a> property to improve the results.

Wordlist cannot be set after a factoid is set. This prevents a factoid from referring to a possibly non existent wordlist. Attempting to do so will result in an E_FAIL HRESULT value.

If a string is added to a word list, its capitalized versions are also implicitly added. For instance, adding "hello" implicitly adds "Hello" and "HELLO".

Using words longer than 256 characters will result in an E_POINTER exception when assigning the <b>WordList</b> property to <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a>.




## -see-also




<a href="tablet.iinkrecognizercontext">IInkRecognizerContext</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>



<a href="https://msdn.microsoft.com/d189fd13-ec69-45dc-8be4-fea48f337636">InkWordList Class</a>
 

 

