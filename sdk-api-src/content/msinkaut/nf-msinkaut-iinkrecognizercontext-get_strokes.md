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

# IInkRecognizerContext::get_Strokes


## -description



Gets or sets the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection associated with the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object.



This property is read/write.


## -parameters


## -remarks



You can set the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection more than once. Each time you set the InkStrokes collection, the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object is reset-any ink or results are removed and any prior calls to the <a href="https://msdn.microsoft.com/a384edf8-3b3d-4e0c-b39c-976798457076">EndInkInput Method</a> method are disregarded-and then the new strokes are added.

The <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection can also be set to <b>NULL</b>, which also resets the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object. When the <b>InkRecognizerContext</b> is reset, it keeps any guides, factoids, and other properties which previously had been set on it.

When the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object is reset, any recognition taking place on the background thread is canceled.

To keep the <b>Strokes</b> property of the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object synchronized with an <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object, use the <a href="https://msdn.microsoft.com/46bbdb98-524f-4b4b-95c0-005e71d672f1">InkAdded</a> and <a href="https://msdn.microsoft.com/59ada470-6620-411d-889e-882f41ccea3e">InkDeleted</a> events of the <b>InkDisp</b> object to listen for strokes that should be added or removed from the <b>InkRecognizerContext</b> object. This covers cases where strokes are added to, deleted from, clipped, or split within the <b>InkDisp</b> object.

<div class="alert"><b>Note</b>  Moving, scaling, or other transformations on strokes in the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object do not generate <a href="https://msdn.microsoft.com/46bbdb98-524f-4b4b-95c0-005e71d672f1">InkAdded</a> or <a href="https://msdn.microsoft.com/59ada470-6620-411d-889e-882f41ccea3e">InkDeleted</a> events. Perform the same transformations on the strokes in the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object to keep the <b>Strokes</b> property of the <b>InkRecognizerContext</b> object synchronized.</div>
<div> </div>



## -see-also




<a href="tablet.iinkrecognizercontext">IInkRecognizerContext</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

