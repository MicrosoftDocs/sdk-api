---
UID: NF:dxgi1_6.IDXGIFactory7.UnregisterAdaptersChangedEvent
title: IDXGIFactory7::UnregisterAdaptersChangedEvent (dxgi1_6.h)
description: Unregisters an event to stop receiving notifications when the adapter enumeration state changes.
helpviewer_keywords: ["IDXGIFactory7 interface [DXGI]","UnregisterAdaptersChangedEvent method","IDXGIFactory7.UnregisterAdaptersChangedEvent","IDXGIFactory7::UnregisterAdaptersChangedEvent","UnregisterAdaptersChangedEvent","UnregisterAdaptersChangedEvent method [DXGI]","UnregisterAdaptersChangedEvent method [DXGI]","IDXGIFactory7 interface","direct3ddxgi.idxgifactory7_unregisteradapterschangedevent","dxgi1_6/IDXGIFactory7::UnregisterAdaptersChangedEvent"]
old-location: direct3ddxgi\idxgifactory7_unregisteradapterschangedevent.htm
tech.root: direct3ddxgi
ms.assetid: D118A5F6-CCFB-425C-82E8-18A3D8FAD79C
ms.date: 12/05/2018
ms.keywords: IDXGIFactory7 interface [DXGI],UnregisterAdaptersChangedEvent method, IDXGIFactory7.UnregisterAdaptersChangedEvent, IDXGIFactory7::UnregisterAdaptersChangedEvent, UnregisterAdaptersChangedEvent, UnregisterAdaptersChangedEvent method [DXGI], UnregisterAdaptersChangedEvent method [DXGI],IDXGIFactory7 interface, direct3ddxgi.idxgifactory7_unregisteradapterschangedevent, dxgi1_6/IDXGIFactory7::UnregisterAdaptersChangedEvent
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
 - IDXGIFactory7::UnregisterAdaptersChangedEvent
 - dxgi1_6/IDXGIFactory7::UnregisterAdaptersChangedEvent
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
 - IDXGIFactory7.UnregisterAdaptersChangedEvent
---

# IDXGIFactory7::UnregisterAdaptersChangedEvent


## -description

Unregisters  an event to stop receiving notifications when the adapter enumeration state changes.

## -parameters

### -param dwCookie [in]

A key value for the event to unregister.

## -returns

Returns <b>S_OK</b> if successful; an error code otherwise.

## -see-also

<a href="/windows/desktop/api/dxgi1_6/nn-dxgi1_6-idxgifactory7">IDXGIFactory7</a>



<a href="/windows/desktop/api/dxgi1_6/nf-dxgi1_6-idxgifactory7-registeradapterschangedevent">RegisterAdaptersChangedEvent</a>