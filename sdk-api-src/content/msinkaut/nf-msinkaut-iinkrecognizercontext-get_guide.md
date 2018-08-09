---
UID: NF:msinkaut.IInkRecognizerContext.get_Guide
title: IInkRecognizerContext::get_Guide
author: windows-sdk-content
description: Gets or sets the InkRecognizerGuide to use for ink input.
old-location: tablet\inkrecognizercontext_guide.htm
old-project: tablet
ms.assetid: 706d28c3-fc5d-496a-a957-daf5ba8d47ca
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 706d28c3-fc5d-496a-a957-daf5ba8d47ca, Guide property [Tablet PC], Guide property [Tablet PC],IInkRecognizerContext interface, IInkRecognizerContext interface [Tablet PC],Guide property, IInkRecognizerContext.Guide, IInkRecognizerContext.get_Guide, IInkRecognizerContext::Guide, IInkRecognizerContext::get_Guide, IInkRecognizerContext::putref_Guide, InkRecognizerContext.get_Guide, get_Guide, msinkaut/IInkRecognizerContext::Guide, msinkaut/IInkRecognizerContext::get_Guide, msinkaut/IInkRecognizerContext::putref_Guide, putref_Guide, tablet.inkrecognizercontext_guide
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRecognizerContext.Guide
 - IInkRecognizerContext.get_Guide
 - InkRecognizerContext.get_Guide
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkRecognizerContext::get_Guide


## -description



Gets or sets the <a href="https://msdn.microsoft.com/c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7">InkRecognizerGuide</a> to use for ink input.



This property is read/write.


## -parameters


## -remarks



Setting the <b>Guide</b> property succeeds only if the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection is <b>NULL</b>. You must set the <b>Guide</b> property before you attach the InkStrokes collection to the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> or you must set the InkStrokes collection to <b>NULL</b> and then set the <b>Guide</b> (and possible reattach the InkStrokes collection).

The <a href="https://msdn.microsoft.com/df405aeb-fefd-4bba-9c02-c1865418f76a">InkRecognizerCapabilities</a> enumeration contains the <b>IRC_FreeInput</b>, <b>IRC_LinedInput</b>, and <b>IRC_BoxedInput</b> flags. These flags specify the capabilities of a recognizer, but because they are read only, there is no way to set any of these directly on a <a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer</a> or <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object. The only way to put a recognizer into a specific mode is to set the guide using the <b>Guide</b> property. If you do not set the <b>Guide</b> property, the recognizer defaults to <b>FreeInput</b> mode (if the recognizer is capable of this). Another way to set the recognizer into <b>FreeInput</b> mode is to set the <b>Guide</b> property to a <a href="https://msdn.microsoft.com/c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7">InkRecognizerGuide</a> object that has its <a href="https://msdn.microsoft.com/dfc2848c-6cd6-4dd6-95b6-4097ef641835">Columns</a> property set to zero and its <a href="https://msdn.microsoft.com/5b1204ca-40b0-4752-8294-6f94412e8e7c">Rows</a> property set to zero.

If you set the <b>Guide</b> property to a <a href="https://msdn.microsoft.com/c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7">InkRecognizerGuide</a> object that has its <a href="https://msdn.microsoft.com/dfc2848c-6cd6-4dd6-95b6-4097ef641835">Columns</a> property set to zero and its <a href="https://msdn.microsoft.com/5b1204ca-40b0-4752-8294-6f94412e8e7c">Rows</a> property set to 1 or more, the recognizer is in <a href="https://msdn.microsoft.com/df405aeb-fefd-4bba-9c02-c1865418f76a">IRC_LinedInput</a> mode (if the recognizer is capable of this). The recognizer uses the <b>Rows</b> property to control the number of lines.

If you set the <b>Guide</b> property to a <a href="https://msdn.microsoft.com/c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7">InkRecognizerGuide</a> object that has its <a href="https://msdn.microsoft.com/5b1204ca-40b0-4752-8294-6f94412e8e7c">Rows</a> property set to zero and its <a href="https://msdn.microsoft.com/dfc2848c-6cd6-4dd6-95b6-4097ef641835">Columns</a> property set to 1 or more, the recognizer is in <a href="https://msdn.microsoft.com/df405aeb-fefd-4bba-9c02-c1865418f76a">IRC_LinedInput</a> mode (if the recognizer is capable of this) for vertical writing. The recognizer uses the <b>Columns</b> property to control the number of vertical lines. If the recognizer is capable of this, the <a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer</a> object's <a href="https://msdn.microsoft.com/c8662817-0a33-4828-8de7-c4ce259738a7">Capabilities</a> property returns either <b>IRC_DownAndLeft</b> or <b>IRC_DownAndRight</b>, or both.

If you set the <b>Guide</b> property to a <a href="https://msdn.microsoft.com/c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7">InkRecognizerGuide</a> object that has its <a href="https://msdn.microsoft.com/dfc2848c-6cd6-4dd6-95b6-4097ef641835">Columns</a> property set to 1 or more and its <a href="https://msdn.microsoft.com/5b1204ca-40b0-4752-8294-6f94412e8e7c">Rows</a> property set to 1 or more, the recognizer is in <a href="https://msdn.microsoft.com/df405aeb-fefd-4bba-9c02-c1865418f76a">IRC_BoxedInput</a> mode (if the recognizer is capable of this).

If you set the mode to one that is not available from this recognizer, an error is returned.

For information about how to query which capabilities, or modes, are available from a specific recognizer, see the <a href="https://msdn.microsoft.com/c8662817-0a33-4828-8de7-c4ce259738a7">Capabilities</a> property of the <a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer</a> object. In general, recognizers of Latin script support free input and horizontal lined input, recognizers of East Asian characters support free input and boxed input, and the gesture recognizer only supports free input.




## -see-also




<a href="https://msdn.microsoft.com/c8662817-0a33-4828-8de7-c4ce259738a7">Capabilities Property</a>



<a href="https://msdn.microsoft.com/dfc2848c-6cd6-4dd6-95b6-4097ef641835">Columns Property</a>



<a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer Interface</a>



<a href="tablet.iinkrecognizercontext">IInkRecognizerContext</a>



<a href="https://msdn.microsoft.com/df405aeb-fefd-4bba-9c02-c1865418f76a">InkRecognizerCapabilities Enumeration</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>



<a href="https://msdn.microsoft.com/c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7">InkRecognizerGuide Class</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>



<a href="https://msdn.microsoft.com/5b1204ca-40b0-4752-8294-6f94412e8e7c">Rows Property</a>
 

 

