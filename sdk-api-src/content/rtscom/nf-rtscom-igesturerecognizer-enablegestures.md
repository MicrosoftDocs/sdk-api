---
UID: NF:rtscom.IGestureRecognizer.EnableGestures
title: IGestureRecognizer::EnableGestures (rtscom.h)
description: Sets a value that indicates to which application gestures the GestureRecognizer Class object responds.
helpviewer_keywords: ["59d39c2c-1c92-4325-b534-36b97a7df20f","EnableGestures","EnableGestures method [Tablet PC]","EnableGestures method [Tablet PC]","IGestureRecognizer interface","IGestureRecognizer interface [Tablet PC]","EnableGestures method","IGestureRecognizer.EnableGestures","IGestureRecognizer::EnableGestures","rtscom/IGestureRecognizer::EnableGestures","tablet.igesturerecognizer_enablegestures"]
old-location: tablet\igesturerecognizer_enablegestures.htm
tech.root: tablet
ms.assetid: 59d39c2c-1c92-4325-b534-36b97a7df20f
ms.date: 12/05/2018
ms.keywords: 59d39c2c-1c92-4325-b534-36b97a7df20f, EnableGestures, EnableGestures method [Tablet PC], EnableGestures method [Tablet PC],IGestureRecognizer interface, IGestureRecognizer interface [Tablet PC],EnableGestures method, IGestureRecognizer.EnableGestures, IGestureRecognizer::EnableGestures, rtscom/IGestureRecognizer::EnableGestures, tablet.igesturerecognizer_enablegestures
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
 - IGestureRecognizer::EnableGestures
 - rtscom/IGestureRecognizer::EnableGestures
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
 - IGestureRecognizer.EnableGestures
---

# IGestureRecognizer::EnableGestures


## -description

Sets a value that indicates to which application gestures the <a href="/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a> object responds.

## -parameters

### -param cGestures [in]

 The size of the array to which the <i>pGestures</i> parameter points. Valid values are between 0 and 64, inclusive.

### -param pGestures [in]

An array of the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">InkApplicationGesture Enumeration</a> values that indicates to which application gestures the <a href="/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a> object responds.

## -returns

For a description of return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

You cannot enable <b>AllGestures</b> in conjunction with any other gestures.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>



<a href="/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-igesturerecognizer">IGestureRecognizer</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-igesturerecognizer-get_enabled">IGestureRecognizer::Enabled Property</a>