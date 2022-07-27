---
UID: NF:d3d11.ID3D11Device.CreateCounter
title: ID3D11Device::CreateCounter (d3d11.h)
description: Create a counter object for measuring GPU performance. (ID3D11Device.CreateCounter)
helpviewer_keywords: ["CreateCounter","CreateCounter method [Direct3D 11]","CreateCounter method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","CreateCounter method","ID3D11Device.CreateCounter","ID3D11Device::CreateCounter","ac3cd491-a912-ddaf-0f13-ac5555a100ca","d3d11/ID3D11Device::CreateCounter","direct3d11.id3d11device_createcounter"]
old-location: direct3d11\id3d11device_createcounter.htm
tech.root: direct3d11
ms.assetid: 857111cc-f590-4383-994c-a72402f8a4aa
ms.date: 12/05/2018
ms.keywords: CreateCounter, CreateCounter method [Direct3D 11], CreateCounter method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateCounter method, ID3D11Device.CreateCounter, ID3D11Device::CreateCounter, ac3cd491-a912-ddaf-0f13-ac5555a100ca, d3d11/ID3D11Device::CreateCounter, direct3d11.id3d11device_createcounter
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Device::CreateCounter
 - d3d11/ID3D11Device::CreateCounter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device.CreateCounter
---

# ID3D11Device::CreateCounter


## -description

Create a counter object for measuring GPU performance.

## -parameters

### -param pCounterDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_counter_desc">D3D11_COUNTER_DESC</a>*</b>

Pointer to a counter description (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_counter_desc">D3D11_COUNTER_DESC</a>).

### -param ppCounter [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11counter">ID3D11Counter</a>**</b>

Address of a pointer to a counter (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11counter">ID3D11Counter</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this function succeeds, it will return S_OK. If it fails, possible return values are: S_FALSE, E_OUTOFMEMORY, DXGI_ERROR_UNSUPPORTED, DXGI_ERROR_NONEXCLUSIVE, or E_INVALIDARG.

DXGI_ERROR_UNSUPPORTED is returned whenever the application requests to create a well-known counter, but the current device does not support it.

DXGI_ERROR_NONEXCLUSIVE indicates that another device object is currently using the counters, so they cannot be used by this device at the moment.

E_INVALIDARG is returned whenever an out-of-range well-known or device-dependent counter is requested, or when the simulataneously active counters have been exhausted.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>
