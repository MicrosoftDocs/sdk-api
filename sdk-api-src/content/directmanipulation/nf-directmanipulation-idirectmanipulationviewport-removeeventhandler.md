---
UID: NF:directmanipulation.IDirectManipulationViewport.RemoveEventHandler
title: IDirectManipulationViewport::RemoveEventHandler (directmanipulation.h)
description: Removes an existing event handler from the viewport.
helpviewer_keywords: ["IDirectManipulationViewport interface [Direct Manipulation]","RemoveEventHandler method","IDirectManipulationViewport.RemoveEventHandler","IDirectManipulationViewport::RemoveEventHandler","RemoveEventHandler","RemoveEventHandler method [Direct Manipulation]","RemoveEventHandler method [Direct Manipulation]","IDirectManipulationViewport interface","directmanipulation.idirectmanipulationviewport_removeeventhandler","directmanipulation/IDirectManipulationViewport::RemoveEventHandler"]
old-location: directmanipulation\idirectmanipulationviewport_removeeventhandler.htm
tech.root: directmanipulation
ms.assetid: ea8539c0-2c0e-4259-a104-ecc02a46372a
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],RemoveEventHandler method, IDirectManipulationViewport.RemoveEventHandler, IDirectManipulationViewport::RemoveEventHandler, RemoveEventHandler, RemoveEventHandler method [Direct Manipulation], RemoveEventHandler method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_removeeventhandler, directmanipulation/IDirectManipulationViewport::RemoveEventHandler
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
 - IDirectManipulationViewport::RemoveEventHandler
 - directmanipulation/IDirectManipulationViewport::RemoveEventHandler
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
 - IDirectManipulationViewport.RemoveEventHandler
---

# IDirectManipulationViewport::RemoveEventHandler


## -description

Removes an existing event handler from the viewport.

## -parameters

### -param cookie [in]

A value that was returned by a previous call to <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-addeventhandler">AddEventHandler</a>.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>