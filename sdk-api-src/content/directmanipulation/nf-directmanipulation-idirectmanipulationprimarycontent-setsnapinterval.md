---
UID: NF:directmanipulation.IDirectManipulationPrimaryContent.SetSnapInterval
title: IDirectManipulationPrimaryContent::SetSnapInterval (directmanipulation.h)
description: Specifies snap points for the inertia end position at uniform intervals.
helpviewer_keywords: ["IDirectManipulationPrimaryContent interface [Direct Manipulation]","SetSnapInterval method","IDirectManipulationPrimaryContent.SetSnapInterval","IDirectManipulationPrimaryContent::SetSnapInterval","SetSnapInterval","SetSnapInterval method [Direct Manipulation]","SetSnapInterval method [Direct Manipulation]","IDirectManipulationPrimaryContent interface","directmanipulation.idirectmanipulationprimarycontent_setsnapinterval","directmanipulation/IDirectManipulationPrimaryContent::SetSnapInterval"]
old-location: directmanipulation\idirectmanipulationprimarycontent_setsnapinterval.htm
tech.root: directmanipulation
ms.assetid: 99d039fe-017a-47c5-95a1-5000efe92ba0
ms.date: 12/05/2018
ms.keywords: IDirectManipulationPrimaryContent interface [Direct Manipulation],SetSnapInterval method, IDirectManipulationPrimaryContent.SetSnapInterval, IDirectManipulationPrimaryContent::SetSnapInterval, SetSnapInterval, SetSnapInterval method [Direct Manipulation], SetSnapInterval method [Direct Manipulation],IDirectManipulationPrimaryContent interface, directmanipulation.idirectmanipulationprimarycontent_setsnapinterval, directmanipulation/IDirectManipulationPrimaryContent::SetSnapInterval
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
 - IDirectManipulationPrimaryContent::SetSnapInterval
 - directmanipulation/IDirectManipulationPrimaryContent::SetSnapInterval
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
 - IDirectManipulationPrimaryContent.SetSnapInterval
---

# IDirectManipulationPrimaryContent::SetSnapInterval


## -description

    Specifies snap points for the inertia end position at uniform intervals.

## -parameters

### -param motion [in]

One of the <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_motion_types">DIRECTMANIPULATION_MOTION_TYPES</a> enumeration values.

### -param interval [in]

The interval between each snap point.

### -param offset [in]

The offset from the coordinate specified in <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate">SetSnapCoordinate</a>.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Snap point locations are in content coordinate units. 

Specify snap points through <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnappoints">SetSnapPoints</a> or <b>SetSnapInterval</b>. 

If snap points are invalid (for example, outside of the content boundaries), they are ignored and the content is always within the content boundaries. 

Snap points are not at boundaries by default. If you wish for content to stop at a boundary, a snap point must be set at the boundary.

 Snap points set by <b>SetSnapInterval</b> can be cleared by calling <b>SetSnapInterval</b> with an interval of 0.0f.


#### Examples

The following example shows how to set the coordinate system for X translation snap points to the origin. Snap points are set every 45 pixels, beginning at the origin along the X-axis.


```
HRESULT hr = SetSnapCoordinate(testWindow, 0, DIRECTMANIPULATION_MOTION_TRANSLATEX, DIRECTMANIPULATION_COORDINATE_ORIGIN, 0.0f);
hr = pContent->SetSnapInterval(DIRECTMANIPULATION_MOTION_TRANSLATEX, 45.0f, 0.0f);
```

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationprimarycontent">IDirectManipulationPrimaryContent</a>



<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate">SetSnapCoordinate</a>



<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnappoints">SetSnapPoints</a>