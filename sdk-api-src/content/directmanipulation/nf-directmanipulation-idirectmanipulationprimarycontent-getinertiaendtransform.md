---
UID: NF:directmanipulation.IDirectManipulationPrimaryContent.GetInertiaEndTransform
title: IDirectManipulationPrimaryContent::GetInertiaEndTransform (directmanipulation.h)
description: Gets the final transform, including inertia, of the primary content.
helpviewer_keywords: ["GetInertiaEndTransform","GetInertiaEndTransform method [Direct Manipulation]","GetInertiaEndTransform method [Direct Manipulation]","IDirectManipulationPrimaryContent interface","IDirectManipulationPrimaryContent interface [Direct Manipulation]","GetInertiaEndTransform method","IDirectManipulationPrimaryContent.GetInertiaEndTransform","IDirectManipulationPrimaryContent::GetInertiaEndTransform","directmanipulation.idirectmanipulationprimarycontent_getinertiaendtransform","directmanipulation/IDirectManipulationPrimaryContent::GetInertiaEndTransform"]
old-location: directmanipulation\idirectmanipulationprimarycontent_getinertiaendtransform.htm
tech.root: directmanipulation
ms.assetid: BCF0E48F-C47E-42BE-90F8-25737301DC9C
ms.date: 12/05/2018
ms.keywords: GetInertiaEndTransform, GetInertiaEndTransform method [Direct Manipulation], GetInertiaEndTransform method [Direct Manipulation],IDirectManipulationPrimaryContent interface, IDirectManipulationPrimaryContent interface [Direct Manipulation],GetInertiaEndTransform method, IDirectManipulationPrimaryContent.GetInertiaEndTransform, IDirectManipulationPrimaryContent::GetInertiaEndTransform, directmanipulation.idirectmanipulationprimarycontent_getinertiaendtransform, directmanipulation/IDirectManipulationPrimaryContent::GetInertiaEndTransform
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
 - IDirectManipulationPrimaryContent::GetInertiaEndTransform
 - directmanipulation/IDirectManipulationPrimaryContent::GetInertiaEndTransform
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
 - IDirectManipulationPrimaryContent.GetInertiaEndTransform
---

# IDirectManipulationPrimaryContent::GetInertiaEndTransform


## -description

Gets the final transform, including inertia, of the primary content.

## -parameters

### -param matrix [out]

The transformed matrix that represents the inertia ending position.

### -param pointCount [in]

The size of the matrix. 

 This value is always 6, because a 3x2 matrix is used for all direct manipulation transforms.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Warning</b>  Calling this method can cause a race condition if inertia has ended or been interrupted. This can also occur during the <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewporteventhandler-onviewportstatuschanged">OnViewportStatusChanged</a> callback.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationprimarycontent">IDirectManipulationPrimaryContent</a>