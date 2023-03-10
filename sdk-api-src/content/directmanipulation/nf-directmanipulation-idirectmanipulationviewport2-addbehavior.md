---
UID: NF:directmanipulation.IDirectManipulationViewport2.AddBehavior
title: IDirectManipulationViewport2::AddBehavior (directmanipulation.h)
description: Adds a behavior to the viewport and returns a cookie to the caller.
helpviewer_keywords: ["AddBehavior","AddBehavior method [Direct Manipulation]","AddBehavior method [Direct Manipulation]","IDirectManipulationViewport2 interface","IDirectManipulationViewport2 interface [Direct Manipulation]","AddBehavior method","IDirectManipulationViewport2.AddBehavior","IDirectManipulationViewport2::AddBehavior","directmanipulation.idirectmanipulationviewport2_addbehavior","directmanipulation/IDirectManipulationViewport2::AddBehavior"]
old-location: directmanipulation\idirectmanipulationviewport2_addbehavior.htm
tech.root: directmanipulation
ms.assetid: E65CF2A3-EF44-4B4E-A8C5-7DC75345B5A6
ms.date: 12/05/2018
ms.keywords: AddBehavior, AddBehavior method [Direct Manipulation], AddBehavior method [Direct Manipulation],IDirectManipulationViewport2 interface, IDirectManipulationViewport2 interface [Direct Manipulation],AddBehavior method, IDirectManipulationViewport2.AddBehavior, IDirectManipulationViewport2::AddBehavior, directmanipulation.idirectmanipulationviewport2_addbehavior, directmanipulation/IDirectManipulationViewport2::AddBehavior
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
 - IDirectManipulationViewport2::AddBehavior
 - directmanipulation/IDirectManipulationViewport2::AddBehavior
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
 - IDirectManipulationViewport2.AddBehavior
---

# IDirectManipulationViewport2::AddBehavior


## -description

Adds a behavior to the viewport and returns a cookie to the caller.

## -parameters

### -param behavior [in]

A behavior created using the <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationmanager2-createbehavior">CreateBehavior</a> method.

### -param cookie [out, retval]

A cookie is returned so the caller can remove this behavior later. This allows the caller to release any reference on the behavior and let <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> maintain an appropriate lifetime, similar to event handlers.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code. Attaching a behavior that is already attached to this viewport or another viewport results in a failure.

## -remarks

A behavior takes effect immediately after <b>AddBehavior</b> is called. This must be considered when adding a behavior during an active manipulation or inertia phase.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport2">IDirectManipulationViewport2</a>