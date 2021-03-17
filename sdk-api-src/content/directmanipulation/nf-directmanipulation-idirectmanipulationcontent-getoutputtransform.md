---
UID: NF:directmanipulation.IDirectManipulationContent.GetOutputTransform
title: IDirectManipulationContent::GetOutputTransform (directmanipulation.h)
description: Gets the final transform applied to the content.
helpviewer_keywords: ["GetOutputTransform","GetOutputTransform method [Direct Manipulation]","GetOutputTransform method [Direct Manipulation]","IDirectManipulationContent interface","IDirectManipulationContent interface [Direct Manipulation]","GetOutputTransform method","IDirectManipulationContent.GetOutputTransform","IDirectManipulationContent::GetOutputTransform","directmanipulation.idirectmanipulationcontent_getoutputtransform","directmanipulation/IDirectManipulationContent::GetOutputTransform"]
old-location: directmanipulation\idirectmanipulationcontent_getoutputtransform.htm
tech.root: directmanipulation
ms.assetid: a8f746a4-650f-4f6d-8734-2e98f01898f2
ms.date: 12/05/2018
ms.keywords: GetOutputTransform, GetOutputTransform method [Direct Manipulation], GetOutputTransform method [Direct Manipulation],IDirectManipulationContent interface, IDirectManipulationContent interface [Direct Manipulation],GetOutputTransform method, IDirectManipulationContent.GetOutputTransform, IDirectManipulationContent::GetOutputTransform, directmanipulation.idirectmanipulationcontent_getoutputtransform, directmanipulation/IDirectManipulationContent::GetOutputTransform
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
 - IDirectManipulationContent::GetOutputTransform
 - directmanipulation/IDirectManipulationContent::GetOutputTransform
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
 - IDirectManipulationContent.GetOutputTransform
---

# IDirectManipulationContent::GetOutputTransform


## -description

Gets the final transform applied to the content.

## -parameters

### -param matrix [out]

The transform matrix.

### -param pointCount [in]

The size of the transform matrix. This value is always 6, because a 3x2 matrix is used for all direct manipulation transforms.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This transform might contain the other custom curves applied during manipulation and inertia.

This transform contains both the content transform and the sync transform set with <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationcontent-synccontenttransform">SyncContentTransform</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcontent">IDirectManipulationContent</a>