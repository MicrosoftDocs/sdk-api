---
UID: NF:windows.graphics.directx.direct3d11.interop.GetInterface
title: ID3D12GraphicsCommandList::GetInterface function (windows.graphics.directx.direct3d11.interop.h)
author: windows-sdk-content
description: Retrieves the DXGI interface that is wrapped by the IDirect3DDxgiInterfaceAccess object.
tech.root: direct3d11
ms.assetid: 7b4d1dcc-407e-4c88-939f-dca0f4ffe027
ms.author: windowssdkdev
ms.date: 04/25/2019
ms.keywords: 7b4d1dcc-407e-4c88-939f-dca0f4ffe027, GetInterface, GetInterface function [Direct3D 11], windows.graphics.directx.direct3d11.interop/GetInterface, direct3d11.getinterface
ms.topic: function
req.header: windows.graphics.directx.direct3d11.interop.h
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
req.dll: D3D11.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D11.dll
api_name:
 - GetInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetInterface function

## -description

Retrieves the DXGI interface that is wrapped by the IDirect3DDxgiInterfaceAccess object.

## -parameters

### -param iid [in]

Type: **REFIID**

A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in p.

### -param p [out]

Type: **void\*\***

A pointer to a memory block that receives a pointer to the the DXGI interface.

## -returns
Type: [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

## -see-also

[Core interfaces](/windows/desktop/direct3d12/direct3d-12-interfaces)
