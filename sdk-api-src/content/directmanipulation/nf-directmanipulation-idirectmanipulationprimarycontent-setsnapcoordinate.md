---
UID: NF:directmanipulation.IDirectManipulationPrimaryContent.SetSnapCoordinate
title: IDirectManipulationPrimaryContent::SetSnapCoordinate (directmanipulation.h)
description: Specifies the coordinate system for snap points or snap intervals.
helpviewer_keywords: ["IDirectManipulationPrimaryContent interface [Direct Manipulation]","SetSnapCoordinate method","IDirectManipulationPrimaryContent.SetSnapCoordinate","IDirectManipulationPrimaryContent::SetSnapCoordinate","SetSnapCoordinate","SetSnapCoordinate method [Direct Manipulation]","SetSnapCoordinate method [Direct Manipulation]","IDirectManipulationPrimaryContent interface","directmanipulation.idirectmanipulationprimarycontent_setsnapcoordinate","directmanipulation/IDirectManipulationPrimaryContent::SetSnapCoordinate"]
old-location: directmanipulation\idirectmanipulationprimarycontent_setsnapcoordinate.htm
tech.root: directmanipulation
ms.assetid: 3f9afe1b-20f4-45fa-a63b-25b7a0c597af
ms.date: 12/05/2018
ms.keywords: IDirectManipulationPrimaryContent interface [Direct Manipulation],SetSnapCoordinate method, IDirectManipulationPrimaryContent.SetSnapCoordinate, IDirectManipulationPrimaryContent::SetSnapCoordinate, SetSnapCoordinate, SetSnapCoordinate method [Direct Manipulation], SetSnapCoordinate method [Direct Manipulation],IDirectManipulationPrimaryContent interface, directmanipulation.idirectmanipulationprimarycontent_setsnapcoordinate, directmanipulation/IDirectManipulationPrimaryContent::SetSnapCoordinate
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
 - IDirectManipulationPrimaryContent::SetSnapCoordinate
 - directmanipulation/IDirectManipulationPrimaryContent::SetSnapCoordinate
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
 - IDirectManipulationPrimaryContent.SetSnapCoordinate
---

# IDirectManipulationPrimaryContent::SetSnapCoordinate


## -description

    Specifies the coordinate system for snap points or snap intervals.

## -parameters

### -param motion [in]

One of the values from <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_motion_types">DIRECTMANIPULATION_MOTION_TYPES</a>.

### -param coordinate [in]

One of the values from <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_snappoint_coordinate">DIRECTMANIPULATION_SNAPPOINT_COORDINATE</a>. 

If <i>motion</i> is set to translation (<b>DIRECTMANIPULATION_MOTION_TRANSLATEX</b> or <b>DIRECTMANIPULATION_MOTION_TRANSLATEY</b>), all values of <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_snappoint_coordinate">DIRECTMANIPULATION_SNAPPOINT_COORDINATE</a> are valid. 

If <i>motion</i> is set to <b>DIRECTMANIPULATION_MOTION_ZOOM</b>, only <b>DIRECTMANIPULATION_COORDINATE_ORIGIN</b> of <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_snappoint_coordinate">DIRECTMANIPULATION_SNAPPOINT_COORDINATE</a> is valid (<i>origin</i> must be set to 0.0f).

### -param origin [in]

The initial, or starting, snap point. All snap points are relative to this one. Only used when  <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_snappoint_coordinate">DIRECTMANIPULATION_COORDINATE_ORIGIN</a> is set. 

If <i>motion</i> is set to <b>DIRECTMANIPULATION_MOTION_ZOOM</b>, then <i>origin</i> must be set to 0.0f.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The origin is relative to the content boundaries. If no boundary has been set (<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationcontent-setcontentrect">SetContentRect</a> is never called) the default boundaries are (-<a href="/previous-versions/ms858507(v=msdn.10)">FLT_MAX</a>, <a href="/previous-versions/ms858507(v=msdn.10)">FLT_MAX</a>).

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationprimarycontent">IDirectManipulationPrimaryContent</a>



<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapinterval">SetSnapInterval</a>



<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnappoints">SetSnapPoints</a>