---
UID: NF:d3d10.ID3D10Device.CreateCounter
title: ID3D10Device::CreateCounter (d3d10.h)
description: Create a counter object for measuring GPU performance. (ID3D10Device.CreateCounter)
helpviewer_keywords: ["225224fa-54a2-8903-494c-754ad030e0af","CreateCounter","CreateCounter method [Direct3D 10]","CreateCounter method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","CreateCounter method","ID3D10Device.CreateCounter","ID3D10Device::CreateCounter","d3d10/ID3D10Device::CreateCounter","direct3d10.id3d10device_createcounter"]
old-location: direct3d10\id3d10device_createcounter.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createcounter.htm
ms.date: 12/05/2018
ms.keywords: 225224fa-54a2-8903-494c-754ad030e0af, CreateCounter, CreateCounter method [Direct3D 10], CreateCounter method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateCounter method, ID3D10Device.CreateCounter, ID3D10Device::CreateCounter, d3d10/ID3D10Device::CreateCounter, direct3d10.id3d10device_createcounter
req.header: d3d10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::CreateCounter
 - d3d10/ID3D10Device::CreateCounter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.CreateCounter
---

# ID3D10Device::CreateCounter


## -description

Create a counter object for measuring GPU performance.

## -parameters

### -param pCounterDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_counter_desc">D3D10_COUNTER_DESC</a>*</b>

Pointer to a counter description (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_counter_desc">D3D10_COUNTER_DESC</a>).

### -param ppCounter [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10counter">ID3D10Counter</a>**</b>

Address of a pointer to a counter (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10counter">ID3D10Counter Interface</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this function succeeds, it will return S_OK. If it fails, possible return values are: S_FALSE, E_OUTOFMEMORY, DXGI_ERROR_UNSUPPORTED, DXGI_ERROR_NONEXCLUSIVE, or E_INVALIDARG.

DXGI_ERROR_UNSUPPORTED is returned whenever the application requests to create a well-known counter, but the current device does not support it.

DXGI_ERROR_NONEXCLUSIVE indicates that another device object is currently using the counters, so they cannot be used by this device at the moment.

E_INVALIDARG is returned whenever an out-of-range well-known or device-dependent counter is requested, or when the simulataneously active counters have been exhausted.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
