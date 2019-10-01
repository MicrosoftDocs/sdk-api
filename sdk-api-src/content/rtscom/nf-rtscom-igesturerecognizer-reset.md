---
UID: NF:rtscom.IGestureRecognizer.Reset
title: IGestureRecognizer::Reset (rtscom.h)
author: windows-sdk-content
description: Deletes past stroke information from the GestureRecognizer Class object.
old-location: tablet\igesturerecognizer_reset.htm
tech.root: tablet
ms.assetid: 05676701-2977-453f-b2b9-7a256899e2b1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 05676701-2977-453f-b2b9-7a256899e2b1, IGestureRecognizer interface [Tablet PC],Reset method, IGestureRecognizer.Reset, IGestureRecognizer::Reset, Reset, Reset method [Tablet PC], Reset method [Tablet PC],IGestureRecognizer interface, rtscom/IGestureRecognizer::Reset, tablet.igesturerecognizer_reset
ms.topic: method
f1_keywords: 
 - "rtscom/IGestureRecognizer.Reset"
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
 - IGestureRecognizer.Reset
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGestureRecognizer::Reset


## -description



Deletes past stroke information from the <a href="https://docs.microsoft.com/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a> object.




## -parameters






## -returns



For a description of return values see <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.




## -remarks



Removes any past strokes from consideration for gestures. If Reset is called while the user is in the middle of writing a stroke, the <a href="https://docs.microsoft.com/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a> object ignores that stroke.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-igesturerecognizer">IGestureRecognizer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-igesturerecognizer-get_enabled">IGestureRecognizer::Enabled Property</a>
 

 

