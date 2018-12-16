---
UID: NF:rtscom.IGestureRecognizer.get_MaxStrokeCount
title: IGestureRecognizer::get_MaxStrokeCount
author: windows-sdk-content
description: Gets or sets the maximum number of strokes allowed per gesture recognition.
old-location: tablet\igesturerecognizer_maxstrokecount.htm
tech.root: tablet
ms.assetid: d7f40294-437a-4d5c-9389-1798102d0d8f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IGestureRecognizer interface [Tablet PC],MaxStrokeCount property, IGestureRecognizer.MaxStrokeCount, IGestureRecognizer.get_MaxStrokeCount, IGestureRecognizer.put_MaxStrokeCount, IGestureRecognizer::MaxStrokeCount, IGestureRecognizer::get_MaxStrokeCount, IGestureRecognizer::put_MaxStrokeCount, MaxStrokeCount property [Tablet PC], MaxStrokeCount property [Tablet PC],IGestureRecognizer interface, d7f40294-437a-4d5c-9389-1798102d0d8f, get_MaxStrokeCount, rtscom/IGestureRecognizer::MaxStrokeCount, rtscom/IGestureRecognizer::get_MaxStrokeCount, rtscom/IGestureRecognizer::put_MaxStrokeCount, tablet.igesturerecognizer_maxstrokecount
ms.topic: method
req.header: rtscom.h
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
req.lib: 
req.dll: RTSCom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IGestureRecognizer.MaxStrokeCount
 - IGestureRecognizer.get_MaxStrokeCount
 - IGestureRecognizer.put_MaxStrokeCount
 - IGestureRecognizer.get_MaxStrokeCount
 - IGestureRecognizer.put_MaxStrokeCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGestureRecognizer::get_MaxStrokeCount


## -description



Gets or sets the maximum number of strokes allowed per gesture recognition.



This property is read/write.


## -parameters


## -remarks



Valid values are 1 and 2. When the <b>MaxStrokeCount</b> property is 2, gesture recognizer looks back to the most recent two strokes and attempts to recognize them as gestures. This may result in multiple recognition calls and multiple gesture events flowing through the system.




## -see-also




<a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a>



<a href="https://msdn.microsoft.com/7cdaf3bf-7aae-4d36-af1c-0eb5a726f388">GestureRecognizer Class</a>



<a href="https://msdn.microsoft.com/dfdc00d6-c843-4298-9773-92775406fbf7">IGestureRecognizer</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>
 

 

