---
UID: NF:d3d9.IDirect3D9.GetAdapterMonitor
title: IDirect3D9::GetAdapterMonitor (d3d9.h)
description: The IDirect3D9::GetAdapterMonitor method (d3d9.h) returns the handle of the monitor associated with the Direct3D object.
helpviewer_keywords: ["1cf647c6-38ba-6d39-fbf9-c82f611d7078","GetAdapterMonitor","GetAdapterMonitor method [Direct3D 9]","GetAdapterMonitor method [Direct3D 9]","IDirect3D9 interface","IDirect3D9 interface [Direct3D 9]","GetAdapterMonitor method","IDirect3D9.GetAdapterMonitor","IDirect3D9::GetAdapterMonitor","d3d9helper/IDirect3D9::GetAdapterMonitor","direct3d9.idirect3d9__getadaptermonitor"]
old-location: direct3d9\idirect3d9__getadaptermonitor.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9__getadaptermonitor.htm
ms.date: 08/10/2022
ms.keywords: 1cf647c6-38ba-6d39-fbf9-c82f611d7078, GetAdapterMonitor, GetAdapterMonitor method [Direct3D 9], GetAdapterMonitor method [Direct3D 9],IDirect3D9 interface, IDirect3D9 interface [Direct3D 9],GetAdapterMonitor method, IDirect3D9.GetAdapterMonitor, IDirect3D9::GetAdapterMonitor, d3d9helper/IDirect3D9::GetAdapterMonitor, direct3d9.idirect3d9__getadaptermonitor
req.header: d3d9.h
req.include-header: D3D9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3D9::GetAdapterMonitor
 - d3d9/IDirect3D9::GetAdapterMonitor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3D9.GetAdapterMonitor
---

# IDirect3D9::GetAdapterMonitor


## -description

Returns the handle of the monitor associated with the Direct3D object.

## -parameters

### -param Adapter [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Ordinal number that denotes the display adapter. D3DADAPTER_DEFAULT is always the primary display adapter.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HMONITOR</a></b>

Handle of the monitor associated with the Direct3D object.

## -remarks

As shown in the following code fragment, which illustrates how to obtain a handle to the monitor associated with a given device, use <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdirect3d">GetDirect3D</a> to return the Direct3D enumerator from the device and use <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getcreationparameters">GetCreationParameters</a> to retrieve the value for Adapter.


```

    if( FAILED( pDevice->GetCreationParameters(  &Parameters ) ) )
        return D3DERR_INVALIDCALL;
    
    if( FAILED( pDevice->GetDirect3D(&pD3D) ) )
        return D3DERR_INVALIDCALL;
    
    hMonitor = pD3D->GetAdapterMonitor(Parameters.AdapterOrdinal);
    
    pD3D->Release();

```

## -see-also

<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getcreationparameters">GetCreationParameters</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdirect3d">GetDirect3D</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3d9">IDirect3D9</a>
