---
UID: NF:msinkaut.IInkRecognizerContext.put_Factoid
title: IInkRecognizerContext::put_Factoid
author: windows-sdk-content
description: Gets or sets the factoid that a recognizer uses to constrain its search for the recognition result.
old-location: tablet\inkrecognizercontext_factoid.htm
tech.root: tablet
ms.assetid: 11a76706-e2e5-4ae5-bdc2-5354514ea29f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 11a76706-e2e5-4ae5-bdc2-5354514ea29f, Factoid property [Tablet PC], Factoid property [Tablet PC],IInkRecognizerContext interface, IInkRecognizerContext interface [Tablet PC],Factoid property, IInkRecognizerContext.Factoid, IInkRecognizerContext.put_Factoid, IInkRecognizerContext::Factoid, IInkRecognizerContext::get_Factoid, IInkRecognizerContext::put_Factoid, InkRecognizerContext.get_Factoid, InkRecognizerContext.put_Factoid, get_Factoid, msinkaut/IInkRecognizerContext::Factoid, msinkaut/IInkRecognizerContext::get_Factoid, msinkaut/IInkRecognizerContext::put_Factoid, put_Factoid, tablet.inkrecognizercontext_factoid
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
 - IInkRecognizerContext.Factoid
 - IInkRecognizerContext.get_Factoid
 - IInkRecognizerContext.put_Factoid
 - InkRecognizerContext.get_Factoid
 - InkRecognizerContext.put_Factoid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkRecognizerContext::put_Factoid


## -description



Gets or sets the factoid that a recognizer uses to constrain its search for the recognition result.



This property is read/write.


## -parameters


## -remarks



A factoid provides recognizer context for recognized ink in the context of a particular field. You specify a factoid if an input field is of a known type, for example, if the input field contains a date.

For more information about factoids and how to use them, see <a href="https://msdn.microsoft.com/b64f6856-453c-4080-84e0-0a9e69e79de7">Improving Tablet PC Recognition Accuracy by Setting Context</a>.

Setting the <b>Factoid</b> succeeds only if the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection is <b>NULL</b>. You must set the <b>Factoid</b> before you attach the InkStrokes collection to the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> or you must set the Strokes collection to <b>NULL</b> and then set the <b>Factoid</b> (and possibly reattach the InkStrokes collection).

To ensure that ink is recognized in the correct field context, set this property before processing the ink for the first time, such as before calling the <a href="https://msdn.microsoft.com/83695dfd-3634-47e7-8311-7216876a827a">Recognize</a> method.

<div class="alert"><b>Note</b>  All factoids are case sensitive.</div>
<div> </div>
This property takes or returns a string parameter and not a class object of the <a href="https://msdn.microsoft.com/247a1f7d-8205-4e4d-9cfc-daad9bd2191f">Factoid</a> class. The members of this class are of type <b>string</b>.

For the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control, this property should only be changed if the <a href="https://msdn.microsoft.com/47a41d5c-2598-4dfc-a5b5-af4df7fdaa6d">Status</a> property returns <a href="https://msdn.microsoft.com/94c3a863-4c8a-4471-be1b-b4d5f8ded374">IES_Idle</a>.




## -see-also




<a href="https://msdn.microsoft.com/247a1f7d-8205-4e4d-9cfc-daad9bd2191f">Factoid Constants</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846801(v=VS.85).aspx">IInkRecognizerContext</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>
 

 

