---
UID: NF:rtscom.IGestureRecognizer.Reset
title: IGestureRecognizer::Reset (rtscom.h)
description: Deletes past stroke information from the GestureRecognizer Class object.
helpviewer_keywords: ["05676701-2977-453f-b2b9-7a256899e2b1","IGestureRecognizer interface [Tablet PC]","Reset method","IGestureRecognizer.Reset","IGestureRecognizer::Reset","Reset","Reset method [Tablet PC]","Reset method [Tablet PC]","IGestureRecognizer interface","rtscom/IGestureRecognizer::Reset","tablet.igesturerecognizer_reset"]
old-location: tablet\igesturerecognizer_reset.htm
tech.root: tablet
ms.assetid: 05676701-2977-453f-b2b9-7a256899e2b1
ms.date: 12/05/2018
ms.keywords: 05676701-2977-453f-b2b9-7a256899e2b1, IGestureRecognizer interface [Tablet PC],Reset method, IGestureRecognizer.Reset, IGestureRecognizer::Reset, Reset, Reset method [Tablet PC], Reset method [Tablet PC],IGestureRecognizer interface, rtscom/IGestureRecognizer::Reset, tablet.igesturerecognizer_reset
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
 - IGestureRecognizer::Reset
 - rtscom/IGestureRecognizer::Reset
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
 - IGestureRecognizer.Reset
---

# IGestureRecognizer::Reset


## -description

Deletes past stroke information from the <a href="/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a> object.



## -returns

For a description of return values see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

Removes any past strokes from consideration for gestures. If Reset is called while the user is in the middle of writing a stroke, the <a href="/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a> object ignores that stroke.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>



<a href="/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-igesturerecognizer">IGestureRecognizer</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-igesturerecognizer-get_enabled">IGestureRecognizer::Enabled Property</a>
