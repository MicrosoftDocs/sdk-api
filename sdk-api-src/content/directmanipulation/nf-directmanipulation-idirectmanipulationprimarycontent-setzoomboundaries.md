---
UID: NF:directmanipulation.IDirectManipulationPrimaryContent.SetZoomBoundaries
title: IDirectManipulationPrimaryContent::SetZoomBoundaries
author: windows-sdk-content
description: Specifies the minimum and maximum boundaries for zoom.
old-location: directmanipulation\idirectmanipulationprimarycontent_setzoomboundaries.htm
old-project: directmanipulation
ms.assetid: 77e4054b-637f-4cff-bfab-0e2a0e992c59
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IDirectManipulationPrimaryContent interface [Direct Manipulation],SetZoomBoundaries method, IDirectManipulationPrimaryContent.SetZoomBoundaries, IDirectManipulationPrimaryContent::SetZoomBoundaries, SetZoomBoundaries, SetZoomBoundaries method [Direct Manipulation], SetZoomBoundaries method [Direct Manipulation],IDirectManipulationPrimaryContent interface, directmanipulation.idirectmanipulationprimarycontent_setzoomboundaries, directmanipulation/IDirectManipulationPrimaryContent::SetZoomBoundaries
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationPrimaryContent.SetZoomBoundaries
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationPrimaryContent::SetZoomBoundaries


## -description


Specifies the minimum and maximum boundaries for zoom.


## -parameters




### -param zoomMinimum [in]

The minimum zoom level allowed. Must be greater than or equal to 0.1f, which corresponds to 100% zoom.


### -param zoomMaximum [in]

The maximum zoom allowed. Must be greater than <i>zoomMinimum</i> and less than <a href="_pluslang_Floating_Limits">FLT_MAX</a>.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



If the content is outside the new boundaries, and the viewport is ENABLED or READY, then the content is reset to be within the new boundaries. If inertia configuration is enabled, the reset operation uses an inertia animation. 




## -see-also




<a href="https://msdn.microsoft.com/9910F5F5-950F-4099-9808-B46FA5BBA6FB">IDirectManipulationPrimaryContent</a>
 

 

