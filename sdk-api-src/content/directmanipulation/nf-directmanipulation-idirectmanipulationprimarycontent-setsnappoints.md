---
UID: NF:directmanipulation.IDirectManipulationPrimaryContent.SetSnapPoints
title: IDirectManipulationPrimaryContent::SetSnapPoints (directmanipulation.h)
description: Specifies the snap points for the inertia rest position.
helpviewer_keywords: ["IDirectManipulationPrimaryContent interface [Direct Manipulation]","SetSnapPoints method","IDirectManipulationPrimaryContent.SetSnapPoints","IDirectManipulationPrimaryContent::SetSnapPoints","SetSnapPoints","SetSnapPoints method [Direct Manipulation]","SetSnapPoints method [Direct Manipulation]","IDirectManipulationPrimaryContent interface","directmanipulation.idirectmanipulationprimarycontent_setsnappoints","directmanipulation/IDirectManipulationPrimaryContent::SetSnapPoints"]
old-location: directmanipulation\idirectmanipulationprimarycontent_setsnappoints.htm
tech.root: directmanipulation
ms.assetid: 3257952d-903b-455c-9422-9739411a5924
ms.date: 12/05/2018
ms.keywords: IDirectManipulationPrimaryContent interface [Direct Manipulation],SetSnapPoints method, IDirectManipulationPrimaryContent.SetSnapPoints, IDirectManipulationPrimaryContent::SetSnapPoints, SetSnapPoints, SetSnapPoints method [Direct Manipulation], SetSnapPoints method [Direct Manipulation],IDirectManipulationPrimaryContent interface, directmanipulation.idirectmanipulationprimarycontent_setsnappoints, directmanipulation/IDirectManipulationPrimaryContent::SetSnapPoints
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
 - IDirectManipulationPrimaryContent::SetSnapPoints
 - directmanipulation/IDirectManipulationPrimaryContent::SetSnapPoints
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
 - IDirectManipulationPrimaryContent.SetSnapPoints
---

# IDirectManipulationPrimaryContent::SetSnapPoints


## -description

Specifies the snap points for the inertia rest position.

## -parameters

### -param motion [in]

One or more of the <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_motion_types">DIRECTMANIPULATION_MOTION_TYPES</a> enumeration values. Only <b>DIRECTMANIPULATION_MOTION_TRANSLATE_X</b>, <b>DIRECTMANIPULATION_MOTION_TRANSLATE_Y</b>, or <b>DIRECTMANIPULATION_MOTION_ZOOM</b> are allowed.

### -param points [in]

An array of snap points within the boundaries of the content to snap to. Should be specified in increasing order relative to the origin set in <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate">SetSnapCoordinate</a>.

### -param pointCount [in]

 The size of the array of snap points. Should be greater than 0.

## -returns

If the method succeeds, it returns <b>S_OK</b>. If there is no change in the snap points, this method can return <b>S_FALSE</b>. Otherwise, it returns an <b>HRESULT</b> error code. If invalid snap points are specified, existing snap points might be affected.

## -remarks

If snap points are invalid (for example, outside of the content boundaries), they are ignored and the content is always within the content boundaries.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationprimarycontent">IDirectManipulationPrimaryContent</a>



<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate">SetSnapCoordinate</a>



<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapinterval">SetSnapInterval</a>