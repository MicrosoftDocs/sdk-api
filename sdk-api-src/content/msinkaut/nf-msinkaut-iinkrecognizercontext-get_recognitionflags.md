---
UID: NF:msinkaut.IInkRecognizerContext.get_RecognitionFlags
title: IInkRecognizerContext::get_RecognitionFlags
author: windows-sdk-content
description: Gets or sets the flags that specify how the recognizer interprets the ink and determines the result string.
old-location: tablet\inkrecognizercontext_recognitionflags.htm
tech.root: tablet
ms.assetid: 71b02f99-4076-4c56-b88a-4201b7033411
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 71b02f99-4076-4c56-b88a-4201b7033411, IInkRecognizerContext interface [Tablet PC],RecognitionFlags property, IInkRecognizerContext.RecognitionFlags, IInkRecognizerContext.get_RecognitionFlags, IInkRecognizerContext::RecognitionFlags, IInkRecognizerContext::get_RecognitionFlags, IInkRecognizerContext::put_RecognitionFlags, InkRecognizerContext.get_RecognitionFlags, InkRecognizerContext.put_RecognitionFlags, RecognitionFlags property [Tablet PC], RecognitionFlags property [Tablet PC],IInkRecognizerContext interface, get_RecognitionFlags, msinkaut/IInkRecognizerContext::RecognitionFlags, msinkaut/IInkRecognizerContext::get_RecognitionFlags, msinkaut/IInkRecognizerContext::put_RecognitionFlags, put_RecognitionFlags, tablet.inkrecognizercontext_recognitionflags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRecognizerContext.RecognitionFlags
 - IInkRecognizerContext.get_RecognitionFlags
 - IInkRecognizerContext.put_RecognitionFlags
 - InkRecognizerContext.get_RecognitionFlags
 - InkRecognizerContext.put_RecognitionFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkRecognizerContext::get_RecognitionFlags


## -description



Gets or sets the flags that specify how the recognizer interprets the ink and determines the result string.



This property is read/write.


## -parameters


## -remarks



The <b>RecognitionFlags</b> property gets or sets flags that specify things such as whether the recognizer treats all ink as a single word or whether the recognizer coerces the result based on the factoid that you specified for the context.

Setting the <b>RecognitionFlags</b> property succeeds only if the <a href="https://msdn.microsoft.com/af31559b-741e-4af2-8c35-9e34ad1af85f">Strokes</a> property is <b>NULL</b>.

For a list of modes that you can use, see the <a href="https://msdn.microsoft.com/ab9f4164-ea07-41d1-be6a-50009fa9464d">InkRecognitionModes</a> enumeration type.

<div class="alert"><b>Note</b>  You can combine modes using the bitwise <b>OR</b> operator.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846801(v=VS.85).aspx">IInkRecognizerContext</a>



<a href="https://msdn.microsoft.com/ab9f4164-ea07-41d1-be6a-50009fa9464d">InkRecognitionModes Enumeration</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>
 

 

