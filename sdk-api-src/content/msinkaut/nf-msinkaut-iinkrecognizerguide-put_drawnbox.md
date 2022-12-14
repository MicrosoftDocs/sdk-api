---
UID: NF:msinkaut.IInkRecognizerGuide.put_DrawnBox
title: IInkRecognizerGuide::put_DrawnBox (msinkaut.h)
description: Gets or sets the box that is physically drawn on the tablet's screen and in which writing takes place. (Put)
helpviewer_keywords: ["DrawnBox property [Tablet PC]","DrawnBox property [Tablet PC]","IInkRecognizerGuide interface","IInkRecognizerGuide interface [Tablet PC]","DrawnBox property","IInkRecognizerGuide.DrawnBox","IInkRecognizerGuide.put_DrawnBox","IInkRecognizerGuide::DrawnBox","IInkRecognizerGuide::get_DrawnBox","IInkRecognizerGuide::put_DrawnBox","InkRecognizerGuide.get_DrawnBox","InkRecognizerGuide.put_DrawnBox","f99095e1-8e7f-47eb-9234-70f651ebf793","msinkaut/IInkRecognizerGuide::DrawnBox","msinkaut/IInkRecognizerGuide::get_DrawnBox","msinkaut/IInkRecognizerGuide::put_DrawnBox","put_DrawnBox","tablet.inkrecognizerguide_drawnbox"]
old-location: tablet\inkrecognizerguide_drawnbox.htm
tech.root: tablet
ms.assetid: f99095e1-8e7f-47eb-9234-70f651ebf793
ms.date: 12/05/2018
ms.keywords: DrawnBox property [Tablet PC], DrawnBox property [Tablet PC],IInkRecognizerGuide interface, IInkRecognizerGuide interface [Tablet PC],DrawnBox property, IInkRecognizerGuide.DrawnBox, IInkRecognizerGuide.put_DrawnBox, IInkRecognizerGuide::DrawnBox, IInkRecognizerGuide::get_DrawnBox, IInkRecognizerGuide::put_DrawnBox, InkRecognizerGuide.get_DrawnBox, InkRecognizerGuide.put_DrawnBox, f99095e1-8e7f-47eb-9234-70f651ebf793, msinkaut/IInkRecognizerGuide::DrawnBox, msinkaut/IInkRecognizerGuide::get_DrawnBox, msinkaut/IInkRecognizerGuide::put_DrawnBox, put_DrawnBox, tablet.inkrecognizerguide_drawnbox
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
 - IInkRecognizerGuide::put_DrawnBox
 - msinkaut/IInkRecognizerGuide::put_DrawnBox
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
 - IInkRecognizerGuide.DrawnBox
 - IInkRecognizerGuide.get_DrawnBox
 - IInkRecognizerGuide.put_DrawnBox
 - InkRecognizerGuide.get_DrawnBox
 - InkRecognizerGuide.put_DrawnBox
---

# IInkRecognizerGuide::put_DrawnBox


## -description

Gets or sets the box that is physically drawn on the tablet's screen and in which writing takes place.



This property is read/write.

## -parameters

## -remarks

The lines of the drawn box are visual cues that specify where writing can take place. The user normally writes within the boundaries of the lines.

Another box, the writing box, is the invisible box in which writing can actually take place. It is larger than the drawn box and provides a margin of error to users if they draw ink outside the lines of the drawn box. You can use the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox">WritingBox</a> property to set the writing box.

The writing box specifies the boundaries of the ink to the recognizer.The drawn box is drawn using ink space  units, relative to the top left of the writing box.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkrecognizerguide.md">IInkRecognizerGuide</a>



<a href="/windows/desktop/tablet/inkrecognizerguide-class">InkRecognizerGuide Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox">WritingBox Property</a>
