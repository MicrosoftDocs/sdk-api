---
UID: NF:windows.graphics.directx.direct3d11.interop.GetDXGIInterfaceFromObject
title: GetDXGIInterfaceFromObject
description: Retrieves a DXGI interface from an object.
helpviewer_keywords: ["interop::GetDXGIInterfaceFromObject"]
tech.root: winrt
ms.assetid: D6C4A15E-7E26-4289-ABF8-254656FFB864
ms.date: 05/13/2019
ms.keywords: interop::GetDXGIInterfaceFromObject
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
 - GetDXGIInterfaceFromObject
 - windows.graphics.directx.direct3d11.interop/GetDXGIInterfaceFromObject
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
 - interop::GetDXGIInterfaceFromObject
---

## -description

Retrieves a DXGI interface from an object.

## -parameters

### -param object

Type: **Platform::Object\^**

The object to retrieve the DXGI interface from.

### -param iid

Type: **REFIID**

The ID of the interface to retrieve.

### -param p

Type: **void\*\***

On return, contains the retrieved DXGI interface.

## -returns

Type: [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

## -remarks

## -see-also

