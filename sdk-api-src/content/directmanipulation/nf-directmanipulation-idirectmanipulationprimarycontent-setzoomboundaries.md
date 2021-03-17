---
UID: NF:directmanipulation.IDirectManipulationPrimaryContent.SetZoomBoundaries
title: IDirectManipulationPrimaryContent::SetZoomBoundaries (directmanipulation.h)
description: Specifies the minimum and maximum boundaries for zoom.
helpviewer_keywords: ["IDirectManipulationPrimaryContent interface [Direct Manipulation]","SetZoomBoundaries method","IDirectManipulationPrimaryContent.SetZoomBoundaries","IDirectManipulationPrimaryContent::SetZoomBoundaries","SetZoomBoundaries","SetZoomBoundaries method [Direct Manipulation]","SetZoomBoundaries method [Direct Manipulation]","IDirectManipulationPrimaryContent interface","directmanipulation.idirectmanipulationprimarycontent_setzoomboundaries","directmanipulation/IDirectManipulationPrimaryContent::SetZoomBoundaries"]
old-location: directmanipulation\idirectmanipulationprimarycontent_setzoomboundaries.htm
tech.root: directmanipulation
ms.assetid: 77e4054b-637f-4cff-bfab-0e2a0e992c59
ms.date: 12/05/2018
ms.keywords: IDirectManipulationPrimaryContent interface [Direct Manipulation],SetZoomBoundaries method, IDirectManipulationPrimaryContent.SetZoomBoundaries, IDirectManipulationPrimaryContent::SetZoomBoundaries, SetZoomBoundaries, SetZoomBoundaries method [Direct Manipulation], SetZoomBoundaries method [Direct Manipulation],IDirectManipulationPrimaryContent interface, directmanipulation.idirectmanipulationprimarycontent_setzoomboundaries, directmanipulation/IDirectManipulationPrimaryContent::SetZoomBoundaries
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectManipulationPrimaryContent::SetZoomBoundaries
 - directmanipulation/IDirectManipulationPrimaryContent::SetZoomBoundaries
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationPrimaryContent.SetZoomBoundaries
---

# IDirectManipulationPrimaryContent::SetZoomBoundaries


## -description

Specifies the minimum and maximum boundaries for zoom.

## -parameters

### -param zoomMinimum [in]

The minimum zoom level allowed. Must be greater than or equal to 0.1f, which corresponds to 100% zoom.

### -param zoomMaximum [in]

The maximum zoom allowed. Must be greater than <i>zoomMinimum</i> and less than <a href="/previous-versions/ms858507(v=msdn.10)">FLT_MAX</a>.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the content is outside the new boundaries, and the viewport is ENABLED or READY, then the content is reset to be within the new boundaries. If inertia configuration is enabled, the reset operation uses an inertia animation.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationprimarycontent">IDirectManipulationPrimaryContent</a>