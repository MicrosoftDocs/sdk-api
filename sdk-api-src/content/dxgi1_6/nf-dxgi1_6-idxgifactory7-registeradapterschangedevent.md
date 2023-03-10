---
UID: NF:dxgi1_6.IDXGIFactory7.RegisterAdaptersChangedEvent
title: IDXGIFactory7::RegisterAdaptersChangedEvent (dxgi1_6.h)
description: Registers to receive notification of changes whenever the adapter enumeration state changes.
helpviewer_keywords: ["IDXGIFactory7 interface [DXGI]","RegisterAdaptersChangedEvent method","IDXGIFactory7.RegisterAdaptersChangedEvent","IDXGIFactory7::RegisterAdaptersChangedEvent","RegisterAdaptersChangedEvent","RegisterAdaptersChangedEvent method [DXGI]","RegisterAdaptersChangedEvent method [DXGI]","IDXGIFactory7 interface","direct3ddxgi.idxgifactory7_registeradapterschangedevent","dxgi1_6/IDXGIFactory7::RegisterAdaptersChangedEvent"]
old-location: direct3ddxgi\idxgifactory7_registeradapterschangedevent.htm
tech.root: direct3ddxgi
ms.assetid: B0A5C04B-B081-4BDD-8952-6CC9116123E0
ms.date: 12/05/2018
ms.keywords: IDXGIFactory7 interface [DXGI],RegisterAdaptersChangedEvent method, IDXGIFactory7.RegisterAdaptersChangedEvent, IDXGIFactory7::RegisterAdaptersChangedEvent, RegisterAdaptersChangedEvent, RegisterAdaptersChangedEvent method [DXGI], RegisterAdaptersChangedEvent method [DXGI],IDXGIFactory7 interface, direct3ddxgi.idxgifactory7_registeradapterschangedevent, dxgi1_6/IDXGIFactory7::RegisterAdaptersChangedEvent
req.header: dxgi1_6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server, version 1709 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxgi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - IDXGIFactory7::RegisterAdaptersChangedEvent
 - dxgi1_6/IDXGIFactory7::RegisterAdaptersChangedEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.lib
 - dxgi.dll
api_name:
 - IDXGIFactory7.RegisterAdaptersChangedEvent
---

# IDXGIFactory7::RegisterAdaptersChangedEvent


## -description

Registers to receive notification of changes whenever the adapter enumeration state changes.

## -parameters

### -param hEvent [in]

A handle to the event object.

### -param pdwCookie [in, out]

A key value for the registered event.

## -returns

Returns <b>S_OK</b> if successful; an error code otherwise.

## -see-also

<a href="/windows/desktop/api/dxgi1_6/nn-dxgi1_6-idxgifactory7">IDXGIFactory7</a>



<a href="/windows/desktop/api/dxgi1_6/nf-dxgi1_6-idxgifactory7-unregisteradapterschangedevent">UnregisterAdaptersChangedEvent</a>