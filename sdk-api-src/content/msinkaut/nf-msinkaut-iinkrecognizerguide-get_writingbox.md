---
UID: NF:msinkaut.IInkRecognizerGuide.get_WritingBox
title: IInkRecognizerGuide::get_WritingBox (msinkaut.h)
description: Gets or sets the invisible writing area of the recognition guide in which writing can actually take place. (Get)
helpviewer_keywords: ["60e37b92-22c2-4a71-a4d1-815226d804fa","IInkRecognizerGuide interface [Tablet PC]","WritingBox property","IInkRecognizerGuide.WritingBox","IInkRecognizerGuide.get_WritingBox","IInkRecognizerGuide::WritingBox","IInkRecognizerGuide::get_WritingBox","IInkRecognizerGuide::put_WritingBox","InkRecognizerGuide.get_WritingBox","InkRecognizerGuide.put_WritingBox","WritingBox property [Tablet PC]","WritingBox property [Tablet PC]","IInkRecognizerGuide interface","get_WritingBox","msinkaut/IInkRecognizerGuide::WritingBox","msinkaut/IInkRecognizerGuide::get_WritingBox","msinkaut/IInkRecognizerGuide::put_WritingBox","put_WritingBox","tablet.inkrecognizerguide_writingbox"]
old-location: tablet\inkrecognizerguide_writingbox.htm
tech.root: tablet
ms.assetid: 60e37b92-22c2-4a71-a4d1-815226d804fa
ms.date: 12/05/2018
ms.keywords: 60e37b92-22c2-4a71-a4d1-815226d804fa, IInkRecognizerGuide interface [Tablet PC],WritingBox property, IInkRecognizerGuide.WritingBox, IInkRecognizerGuide.get_WritingBox, IInkRecognizerGuide::WritingBox, IInkRecognizerGuide::get_WritingBox, IInkRecognizerGuide::put_WritingBox, InkRecognizerGuide.get_WritingBox, InkRecognizerGuide.put_WritingBox, WritingBox property [Tablet PC], WritingBox property [Tablet PC],IInkRecognizerGuide interface, get_WritingBox, msinkaut/IInkRecognizerGuide::WritingBox, msinkaut/IInkRecognizerGuide::get_WritingBox, msinkaut/IInkRecognizerGuide::put_WritingBox, put_WritingBox, tablet.inkrecognizerguide_writingbox
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkRecognizerGuide::get_WritingBox
 - msinkaut/IInkRecognizerGuide::get_WritingBox
dev_langs:
 - c++
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
---

# IInkRecognizerGuide::get_WritingBox


## -description

Gets or sets the invisible writing area of the recognition guide in which writing can actually take place.



This property is read/write.

## -parameters

## -remarks

The writing box provides a margin of error to users who write outside the drawn box-the lines that are physically drawn on the tablet screen within which users write. You can use the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox">DrawnBox</a> property to set the drawn box.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox">DrawnBox Property</a>



<a href="../msinkaut/nn-msinkaut-iinkrecognizerguide.md">IInkRecognizerGuide</a>



<a href="/windows/desktop/tablet/inkrecognizerguide-class">InkRecognizerGuide Class</a>



<a href="/windows/desktop/tablet/inkrectangle-class">InkRectangle Class</a>
