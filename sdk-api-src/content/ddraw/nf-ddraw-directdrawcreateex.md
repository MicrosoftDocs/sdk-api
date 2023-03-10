---
UID: NF:ddraw.DirectDrawCreateEx
title: DirectDrawCreateEx function (ddraw.h)
description: Creates an instance of a DirectDraw object that supports the set of Direct3D interfaces in DirectX 7.0. To use the features of Direct3D in DirectX 7.0, create a DirectDraw object with this function.
helpviewer_keywords: ["DDCREATE_EMULATIONONLY","DDCREATE_HARDWAREONLY","DirectDrawCreateEx","DirectDrawCreateEx function [DirectDraw]","ddraw/DirectDrawCreateEx","directdraw.directdrawcreateex"]
old-location: directdraw\directdrawcreateex.htm
tech.root: directdraw
ms.assetid: 67fa1cd0-e47f-4dc4-b92c-b3401b4cbb57
ms.date: 12/05/2018
ms.keywords: DDCREATE_EMULATIONONLY, DDCREATE_HARDWAREONLY, DirectDrawCreateEx, DirectDrawCreateEx function [DirectDraw], ddraw/DirectDrawCreateEx, directdraw.directdrawcreateex
req.header: ddraw.h
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
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DirectDrawCreateEx
 - ddraw/DirectDrawCreateEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ddraw.dll
 - Ext-MS-Win-DX-DDraw-L1-1-0.dll
api_name:
 - DirectDrawCreateEx
---

# DirectDrawCreateEx function


## -description

Creates an instance of a DirectDraw object that supports the set of Direct3D interfaces in DirectX 7.0. To use the features of Direct3D in DirectX 7.0, create a DirectDraw object with this function.

## -parameters

### -param lpGuid [in]

A pointer to the globally unique identifier (GUID) that represents the driver to be created. This can be NULL to indicate the active display driver, or you can pass one of the following flags to restrict the active display driver's behavior for debugging purposes:



#### DDCREATE_EMULATIONONLY

The DirectDraw object uses emulation for all features; it does not take advantage of any hardware-supported features.



#### DDCREATE_HARDWAREONLY

The DirectDraw object never emulates features not supported by the hardware. Attempts to call methods that require unsupported features fail, returning DDERR_UNSUPPORTED.

### -param lplpDD [out]

A pointer to a variable to be set to a valid <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a> interface pointer if the call succeeds.

### -param iid [in]

This parameter must be set to IID_IDirectDraw7. This function fails and returns DDERR_INVALIDPARAMS if any other interface is specified.

### -param pUnkOuter [in]

Allows for future compatibility with COM aggregation features. Currently, this function returns an error if this parameter is not NULL.

## -returns

If the function succeeds, the return value is DD_OK.



If it fails, the function can return one of the following error values:

<ul>
<li>DDERR_DIRECTDRAWALREADYCREATED</li>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDDIRECTDRAWGUID</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NODIRECTDRAWHW</li>
<li>DDERR_OUTOFMEMORY</li>
</ul>

## -remarks

This function attempts to initialize a DirectDraw object, and then sets a pointer to the object if the call succeeds.

On computers with multiple monitors, if you specify NULL for <i>lpGUID</i>, the DirectDraw object runs in emulation mode when the normal cooperative level is set. To make use of hardware acceleration on these computers, specify the device's GUID.

You must use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to access the <b>DirectDrawCreateEx</b> function.