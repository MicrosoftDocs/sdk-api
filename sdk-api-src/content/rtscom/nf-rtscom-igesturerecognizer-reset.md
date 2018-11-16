---
UID: NF:rtscom.IGestureRecognizer.Reset
title: IGestureRecognizer::Reset
author: windows-sdk-content
description: Deletes past stroke information from the GestureRecognizer Class object.
old-location: tablet\igesturerecognizer_reset.htm
tech.root: tablet
ms.assetid: 05676701-2977-453f-b2b9-7a256899e2b1
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 05676701-2977-453f-b2b9-7a256899e2b1, IGestureRecognizer interface [Tablet PC],Reset method, IGestureRecognizer.Reset, IGestureRecognizer::Reset, Reset, Reset method [Tablet PC], Reset method [Tablet PC],IGestureRecognizer interface, rtscom/IGestureRecognizer::Reset, tablet.igesturerecognizer_reset
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IGestureRecognizer.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- rtscom.h
: 
- IGestureRecognizer.Reset
: 
---

# IGestureRecognizer::Reset


## -description



Deletes past stroke information from the <a href="https://msdn.microsoft.com/7cdaf3bf-7aae-4d36-af1c-0eb5a726f388">GestureRecognizer Class</a> object.




## -parameters






## -returns



For a description of return values see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



Removes any past strokes from consideration for gestures. If Reset is called while the user is in the middle of writing a stroke, the <a href="https://msdn.microsoft.com/7cdaf3bf-7aae-4d36-af1c-0eb5a726f388">GestureRecognizer Class</a> object ignores that stroke.




## -see-also




<a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a>



<a href="https://msdn.microsoft.com/7cdaf3bf-7aae-4d36-af1c-0eb5a726f388">GestureRecognizer Class</a>



<a href="https://msdn.microsoft.com/dfdc00d6-c843-4298-9773-92775406fbf7">IGestureRecognizer</a>



<a href="https://msdn.microsoft.com/4e977348-30d8-474c-80af-56371be5aee4">IGestureRecognizer::Enabled Property</a>
 

 

