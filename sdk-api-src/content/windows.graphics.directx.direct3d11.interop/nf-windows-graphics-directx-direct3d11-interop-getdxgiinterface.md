---
UID: NF:windows.graphics.directx.direct3d11.interop.GetDXGIInterface
title: GetDXGIInterface
description: Retrieves a DXGI interface from an [IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) instance.
helpviewer_keywords: ["interop::GetDXGIInterface"]
tech.root: winrt
ms.assetid: 0D0D158F-5D1E-4386-8131-C6492993F87B
ms.date: 05/13/2019
ms.keywords: interop::GetDXGIInterface
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: D3D11.dll
req.header: windows.graphics.directx.direct3d11.interop.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: D3D11.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
targetos: Windows
f1_keywords:
 - GetDXGIInterface
 - windows.graphics.directx.direct3d11.interop/GetDXGIInterface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D11.dll
api_name:
 - interop::GetDXGIInterface
---

## -description

Retrieves a DXGI interface from an [IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) instance.

## -parameters

### -param device

Type: **[IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice)\^**

The [IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) instance to retrieve the DXGI interface from.

### -param dxgi

Type: **DXGI_TYPE\*\***

On return, contains the retrieved DXGI interface.

## -returns

Type: [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

## -remarks

## -see-also

