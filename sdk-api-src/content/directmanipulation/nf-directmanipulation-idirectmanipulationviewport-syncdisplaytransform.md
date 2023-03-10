---
UID: NF:directmanipulation.IDirectManipulationViewport.SyncDisplayTransform
title: IDirectManipulationViewport::SyncDisplayTransform (directmanipulation.h)
description: Specifies a display transform for the viewport, and synchronizes the output transform with the new value of the display transform.
helpviewer_keywords: ["IDirectManipulationViewport interface [Direct Manipulation]","SyncDisplayTransform method","IDirectManipulationViewport.SyncDisplayTransform","IDirectManipulationViewport::SyncDisplayTransform","SyncDisplayTransform","SyncDisplayTransform method [Direct Manipulation]","SyncDisplayTransform method [Direct Manipulation]","IDirectManipulationViewport interface","directmanipulation.idirectmanipulationviewport_syncdisplaytransform","directmanipulation/IDirectManipulationViewport::SyncDisplayTransform"]
old-location: directmanipulation\idirectmanipulationviewport_syncdisplaytransform.htm
tech.root: directmanipulation
ms.assetid: 0af63d1e-026e-4083-a1b2-56ba31653434
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],SyncDisplayTransform method, IDirectManipulationViewport.SyncDisplayTransform, IDirectManipulationViewport::SyncDisplayTransform, SyncDisplayTransform, SyncDisplayTransform method [Direct Manipulation], SyncDisplayTransform method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_syncdisplaytransform, directmanipulation/IDirectManipulationViewport::SyncDisplayTransform
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
 - IDirectManipulationViewport::SyncDisplayTransform
 - directmanipulation/IDirectManipulationViewport::SyncDisplayTransform
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
 - IDirectManipulationViewport.SyncDisplayTransform
---

# IDirectManipulationViewport::SyncDisplayTransform


## -description

Specifies a display transform for the viewport, and synchronizes the output transform with the new value of the display transform.

## -parameters

### -param matrix [in]

The transform matrix, in row-wise order: _11, _12, _21, _22, _31, _32.

### -param pointCount [in]

The size of the transform matrix. This value is always 6, because a 3x2 matrix is used for all direct manipulation transforms.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the application performs special output processing of the content outside of the compositor (content not fully captured in the viewport transform), it should call this method to specify the display transform for the special processing.


The display transform affects how manipulation updates are applied to the output transform. For example, if the display transform is set to scale 3x, panning will move the content 3x the original distance. 


When a display transform is changed using this method, the output transform will be synchronized to the new value of the display transform.


This method cannot be called if the viewport status is <b>DIRECTMANIPULATION_RUNNING</b> or <b>DIRECTMANIPULATION_INERTIA</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>