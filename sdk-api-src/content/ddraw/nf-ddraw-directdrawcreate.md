---
UID: NF:ddraw.DirectDrawCreate
title: DirectDrawCreate function (ddraw.h)
description: Creates an instance of a DirectDraw object.
helpviewer_keywords: ["DDCREATE_EMULATIONONLY","DDCREATE_HARDWAREONLY","DirectDrawCreate","DirectDrawCreate function [DirectDraw]","ddraw/DirectDrawCreate","directdraw.directdrawcreate"]
old-location: directdraw\directdrawcreate.htm
tech.root: directdraw
ms.assetid: bad18493-417f-499d-a9a8-719d094be62a
ms.date: 12/05/2018
ms.keywords: DDCREATE_EMULATIONONLY, DDCREATE_HARDWAREONLY, DirectDrawCreate, DirectDrawCreate function [DirectDraw], ddraw/DirectDrawCreate, directdraw.directdrawcreate
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
 - DirectDrawCreate
 - ddraw/DirectDrawCreate
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
 - DirectDrawCreate
---

# DirectDrawCreate function


## -description

Creates an instance of a DirectDraw object. A DirectDraw object that is created by using this function does not support the complete set of Direct3D interfaces in DirectX 7.0. To create a DirectDraw object that is capable of exposing all of the features of Direct3D in DirectX 7.0, use the <a href="/windows/desktop/api/ddraw/nf-ddraw-directdrawcreateex">DirectDrawCreateEx</a> function.

## -parameters

### -param lpGUID [in]

A pointer to the globally unique identifier (GUID) that represents the driver to be created. This can be NULL to indicate the active display driver, or you can pass one of the following flags to restrict the active display driver's behavior for debugging purposes:



#### DDCREATE_EMULATIONONLY

The DirectDraw object uses emulation for all features; it does not take advantage of any hardware-supported features.



#### DDCREATE_HARDWAREONLY

The DirectDraw object never emulates features not supported by the hardware. Attempts to call methods that require unsupported features fail, returning DDERR_UNSUPPORTED.

### -param lplpDD [out]

A pointer to a variable to be set to a valid <b>IDirectDraw</b> interface pointer if the call succeeds.

### -param pUnkOuter [in]

Allows for future compatibility with COM aggregation features. Presently, however, this function returns an error if this parameter is anything but NULL.

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

You must use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to access the <b>DirectDrawCreate</b> function.