---
UID: NF:rtscom.IGestureRecognizer.put_MaxStrokeCount
title: IGestureRecognizer::put_MaxStrokeCount (rtscom.h)
description: Gets or sets the maximum number of strokes allowed per gesture recognition. (Put)
helpviewer_keywords: ["IGestureRecognizer interface [Tablet PC]","MaxStrokeCount property","IGestureRecognizer.MaxStrokeCount","IGestureRecognizer.get_MaxStrokeCount","IGestureRecognizer.put_MaxStrokeCount","IGestureRecognizer::MaxStrokeCount","IGestureRecognizer::get_MaxStrokeCount","IGestureRecognizer::put_MaxStrokeCount","MaxStrokeCount property [Tablet PC]","MaxStrokeCount property [Tablet PC]","IGestureRecognizer interface","d7f40294-437a-4d5c-9389-1798102d0d8f","put_MaxStrokeCount","rtscom/IGestureRecognizer::MaxStrokeCount","rtscom/IGestureRecognizer::get_MaxStrokeCount","rtscom/IGestureRecognizer::put_MaxStrokeCount","tablet.igesturerecognizer_maxstrokecount"]
old-location: tablet\igesturerecognizer_maxstrokecount.htm
tech.root: tablet
ms.assetid: d7f40294-437a-4d5c-9389-1798102d0d8f
ms.date: 12/05/2018
ms.keywords: IGestureRecognizer interface [Tablet PC],MaxStrokeCount property, IGestureRecognizer.MaxStrokeCount, IGestureRecognizer.get_MaxStrokeCount, IGestureRecognizer.put_MaxStrokeCount, IGestureRecognizer::MaxStrokeCount, IGestureRecognizer::get_MaxStrokeCount, IGestureRecognizer::put_MaxStrokeCount, MaxStrokeCount property [Tablet PC], MaxStrokeCount property [Tablet PC],IGestureRecognizer interface, d7f40294-437a-4d5c-9389-1798102d0d8f, put_MaxStrokeCount, rtscom/IGestureRecognizer::MaxStrokeCount, rtscom/IGestureRecognizer::get_MaxStrokeCount, rtscom/IGestureRecognizer::put_MaxStrokeCount, tablet.igesturerecognizer_maxstrokecount
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGestureRecognizer::put_MaxStrokeCount
 - rtscom/IGestureRecognizer::put_MaxStrokeCount
dev_langs:
 - c++
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
---

# IGestureRecognizer::put_MaxStrokeCount


## -description

Gets or sets the maximum number of strokes allowed per gesture recognition.



This property is read/write.

## -parameters

## -remarks

Valid values are 1 and 2. When the <b>MaxStrokeCount</b> property is 2, gesture recognizer looks back to the most recent two strokes and attempts to recognize them as gestures. This may result in multiple recognition calls and multiple gesture events flowing through the system.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>



<a href="/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-igesturerecognizer">IGestureRecognizer</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>
