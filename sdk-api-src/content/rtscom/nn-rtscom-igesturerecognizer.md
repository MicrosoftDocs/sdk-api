---
UID: NN:rtscom.IGestureRecognizer
title: IGestureRecognizer (rtscom.h)
description: Reacts to events by recognizing gestures and adding gesture data to the input queue.
helpviewer_keywords: ["IGestureRecognizer","IGestureRecognizer interface [Tablet PC]","IGestureRecognizer interface [Tablet PC]","described","dfdc00d6-c843-4298-9773-92775406fbf7","rtscom/IGestureRecognizer","tablet.igesturerecognizer"]
old-location: tablet\igesturerecognizer.htm
tech.root: tablet
ms.assetid: dfdc00d6-c843-4298-9773-92775406fbf7
ms.date: 12/05/2018
ms.keywords: IGestureRecognizer, IGestureRecognizer interface [Tablet PC], IGestureRecognizer interface [Tablet PC],described, dfdc00d6-c843-4298-9773-92775406fbf7, rtscom/IGestureRecognizer, tablet.igesturerecognizer
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
 - IGestureRecognizer
 - rtscom/IGestureRecognizer
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
 - IGestureRecognizer
---

# IGestureRecognizer interface


## -description

Reacts to events by recognizing gestures and adding gesture data to the input queue.

## -inheritance

The <b>IGestureRecognizer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGestureRecognizer</b> also has these types of members:

## -remarks

This interface is implemented by the <a href="/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a>.

The gesture recognizer analyzes digitizer input and injects gesture recognition results into the input queue.

Adding an instance of the <a href="/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a> to multiple <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> instances is not a valid operation.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>



<a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>
