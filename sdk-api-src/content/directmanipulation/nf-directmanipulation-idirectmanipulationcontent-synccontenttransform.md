---
UID: NF:directmanipulation.IDirectManipulationContent.SyncContentTransform
title: IDirectManipulationContent::SyncContentTransform (directmanipulation.h)
description: Modifies the content transform while maintaining the output transform.
helpviewer_keywords: ["IDirectManipulationContent interface [Direct Manipulation]","SyncContentTransform method","IDirectManipulationContent.SyncContentTransform","IDirectManipulationContent::SyncContentTransform","SyncContentTransform","SyncContentTransform method [Direct Manipulation]","SyncContentTransform method [Direct Manipulation]","IDirectManipulationContent interface","directmanipulation.idirectmanipulationcontent_synccontenttransform","directmanipulation/IDirectManipulationContent::SyncContentTransform"]
old-location: directmanipulation\idirectmanipulationcontent_synccontenttransform.htm
tech.root: directmanipulation
ms.assetid: 3e70b208-05b5-4b84-a582-fd835acdd777
ms.date: 12/05/2018
ms.keywords: IDirectManipulationContent interface [Direct Manipulation],SyncContentTransform method, IDirectManipulationContent.SyncContentTransform, IDirectManipulationContent::SyncContentTransform, SyncContentTransform, SyncContentTransform method [Direct Manipulation], SyncContentTransform method [Direct Manipulation],IDirectManipulationContent interface, directmanipulation.idirectmanipulationcontent_synccontenttransform, directmanipulation/IDirectManipulationContent::SyncContentTransform
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
 - IDirectManipulationContent::SyncContentTransform
 - directmanipulation/IDirectManipulationContent::SyncContentTransform
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
 - IDirectManipulationContent.SyncContentTransform
---

# IDirectManipulationContent::SyncContentTransform


## -description

Modifies the content transform while maintaining the output transform.

## -parameters

### -param matrix [in]

The transform matrix.

### -param pointCount [in]

The size of the transform matrix. This value is always 6, because a 3x2 matrix is used for all direct manipulation transforms.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method will fail if the viewport state is <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_status">DIRECTMANIPULATION_RUNNING</a>, <b>DIRECTMANIPULATION_INERTIA</b> or <b>DIRECTMANIPULATION_SUSPENDED</b>.

This method is useful when the application wants to apply transforms on top of the content transforms at the end of a manipulation, while preserving the visual output transform of the content.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcontent">IDirectManipulationContent</a>