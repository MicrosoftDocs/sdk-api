---
UID: NF:msinkaut.IInkRecognizerGuide.get_DrawnBox
title: IInkRecognizerGuide::get_DrawnBox (msinkaut.h)

description: Gets or sets the box that is physically drawn on the tablet's screen and in which writing takes place.
old-location: tablet\inkrecognizerguide_drawnbox.htm
tech.root: tablet
ms.assetid: f99095e1-8e7f-47eb-9234-70f651ebf793

ms.date: 12/05/2018
ms.keywords: DrawnBox property [Tablet PC], DrawnBox property [Tablet PC],IInkRecognizerGuide interface, IInkRecognizerGuide interface [Tablet PC],DrawnBox property, IInkRecognizerGuide.DrawnBox, IInkRecognizerGuide.get_DrawnBox, IInkRecognizerGuide::DrawnBox, IInkRecognizerGuide::get_DrawnBox, IInkRecognizerGuide::put_DrawnBox, InkRecognizerGuide.get_DrawnBox, InkRecognizerGuide.put_DrawnBox, f99095e1-8e7f-47eb-9234-70f651ebf793, get_DrawnBox, msinkaut/IInkRecognizerGuide::DrawnBox, msinkaut/IInkRecognizerGuide::get_DrawnBox, msinkaut/IInkRecognizerGuide::put_DrawnBox, tablet.inkrecognizerguide_drawnbox
ms.topic: method
f1_keywords: 
 - "msinkaut/IInkRecognizerGuide.DrawnBox"
dev_langs:
 - c++
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
 - IInkRecognizerGuide.DrawnBox
 - IInkRecognizerGuide.get_DrawnBox
 - IInkRecognizerGuide.put_DrawnBox
 - InkRecognizerGuide.get_DrawnBox
 - InkRecognizerGuide.put_DrawnBox
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkRecognizerGuide::get_DrawnBox


## -description



Gets or sets the box that is physically drawn on the tablet's screen and in which writing takes place.



This property is read/write.


## -parameters


## -remarks



The lines of the drawn box are visual cues that specify where writing can take place. The user normally writes within the boundaries of the lines.

Another box, the writing box, is the invisible box in which writing can actually take place. It is larger than the drawn box and provides a margin of error to users if they draw ink outside the lines of the drawn box. You can use the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox">WritingBox</a> property to set the writing box.

The writing box specifies the boundaries of the ink to the recognizer.The drawn box is drawn using ink space  units, relative to the top left of the writing box.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846802(v=VS.85).aspx">IInkRecognizerGuide</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizerguide-class">InkRecognizerGuide Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox">WritingBox Property</a>
 

 

