---
UID: NF:msinkaut.IInkRecognizerGuide.get_WritingBox
title: IInkRecognizerGuide::get_WritingBox
author: windows-sdk-content
description: Gets or sets the invisible writing area of the recognition guide in which writing can actually take place.
old-location: tablet\inkrecognizerguide_writingbox.htm
old-project: tablet
ms.assetid: 60e37b92-22c2-4a71-a4d1-815226d804fa
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 60e37b92-22c2-4a71-a4d1-815226d804fa, IInkRecognizerGuide interface [Tablet PC],WritingBox property, IInkRecognizerGuide.WritingBox, IInkRecognizerGuide.get_WritingBox, IInkRecognizerGuide::WritingBox, IInkRecognizerGuide::get_WritingBox, IInkRecognizerGuide::put_WritingBox, InkRecognizerGuide.get_WritingBox, InkRecognizerGuide.put_WritingBox, WritingBox property [Tablet PC], WritingBox property [Tablet PC],IInkRecognizerGuide interface, get_WritingBox, msinkaut/IInkRecognizerGuide::WritingBox, msinkaut/IInkRecognizerGuide::get_WritingBox, msinkaut/IInkRecognizerGuide::put_WritingBox, put_WritingBox, tablet.inkrecognizerguide_writingbox
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
 - IInkRecognizerGuide.WritingBox
 - IInkRecognizerGuide.get_WritingBox
 - IInkRecognizerGuide.put_WritingBox
 - InkRecognizerGuide.get_WritingBox
 - InkRecognizerGuide.put_WritingBox
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkRecognizerGuide::get_WritingBox


## -description



Gets or sets the invisible writing area of the recognition guide in which writing can actually take place.



This property is read/write.


## -parameters


## -remarks



The writing box provides a margin of error to users who write outside the drawn box-the lines that are physically drawn on the tablet screen within which users write. You can use the <a href="https://msdn.microsoft.com/f99095e1-8e7f-47eb-9234-70f651ebf793">DrawnBox</a> property to set the drawn box.




## -see-also




<a href="https://msdn.microsoft.com/f99095e1-8e7f-47eb-9234-70f651ebf793">DrawnBox Property</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846802(v=VS.85).aspx">IInkRecognizerGuide</a>



<a href="https://msdn.microsoft.com/c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7">InkRecognizerGuide Class</a>



<a href="https://msdn.microsoft.com/78e6c29c-0f43-46a5-9d30-948de5f369c8">InkRectangle Class</a>
 

 

