---
UID: NF:directmanipulation.IDirectManipulationViewport2.RemoveBehavior
title: IDirectManipulationViewport2::RemoveBehavior (directmanipulation.h)
description: Removes a behavior from the viewport that matches the given cookie.
helpviewer_keywords: ["IDirectManipulationViewport2 interface [Direct Manipulation]","RemoveBehavior method","IDirectManipulationViewport2.RemoveBehavior","IDirectManipulationViewport2::RemoveBehavior","RemoveBehavior","RemoveBehavior method [Direct Manipulation]","RemoveBehavior method [Direct Manipulation]","IDirectManipulationViewport2 interface","directmanipulation.idirectmanipulationviewport2_removebehavior","directmanipulation/IDirectManipulationViewport2::RemoveBehavior"]
old-location: directmanipulation\idirectmanipulationviewport2_removebehavior.htm
tech.root: directmanipulation
ms.assetid: CA5FF0FC-6ED9-4964-9751-90387650A198
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewport2 interface [Direct Manipulation],RemoveBehavior method, IDirectManipulationViewport2.RemoveBehavior, IDirectManipulationViewport2::RemoveBehavior, RemoveBehavior, RemoveBehavior method [Direct Manipulation], RemoveBehavior method [Direct Manipulation],IDirectManipulationViewport2 interface, directmanipulation.idirectmanipulationviewport2_removebehavior, directmanipulation/IDirectManipulationViewport2::RemoveBehavior
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IDirectManipulationViewport2::RemoveBehavior
 - directmanipulation/IDirectManipulationViewport2::RemoveBehavior
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
 - IDirectManipulationViewport2.RemoveBehavior
---

# IDirectManipulationViewport2::RemoveBehavior


## -description

Removes a behavior from the viewport that matches the given cookie.

## -parameters

### -param cookie [in]

A valid cookie returned from the <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport2-addbehavior">AddBehavior</a> call on the same viewport.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code. If the behavior has already been removed or if the behavior is not attached to this viewport a failure is returned.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport2">IDirectManipulationViewport2</a>