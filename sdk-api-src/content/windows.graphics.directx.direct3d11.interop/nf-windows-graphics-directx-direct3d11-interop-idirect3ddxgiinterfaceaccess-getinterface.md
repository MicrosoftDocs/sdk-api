---
UID: NF:windows.graphics.directx.direct3d11.interop.IDirect3DDxgiInterfaceAccess.GetInterface
title: IDirect3DDxgiInterfaceAccess::GetInterface method
description: Retrieves the DXGI interface that is wrapped by the IDirect3DDxgiInterfaceAccess object.
helpviewer_keywords: ["GetInterface","GetInterface function [Direct3D 11]","windows.graphics.directx.direct3d11.interop/GetInterface","direct3d11.getinterface"]
tech.root: winrt
ms.assetid: 
ms.date: 05/13/2019
ms.keywords: GetInterface, GetInterface function [Direct3D 11], windows.graphics.directx.direct3d11.interop/GetInterface, direct3d11.getinterface
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
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
targetos: Windows
f1_keywords:
 - IDirect3DDxgiInterfaceAccess::GetInterface
 - windows.graphics.directx.direct3d11.interop/IDirect3DDxgiInterfaceAccess::GetInterface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.dll
api_name:
 - GetInterface
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

A pointer to a memory block that receives a pointer to the DXGI interface.

## -returns

Type: [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

## -see-also

[Core interfaces](/windows/desktop/direct3d12/direct3d-12-interfaces)

