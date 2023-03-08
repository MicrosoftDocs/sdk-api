---
UID: NF:ddraw.DirectDrawEnumerateA
tech.root: directdraw 
title: DirectDrawEnumerateA
ms.date: 04/14/2021
targetos: Windows
description: This function is superseded by the DirectDrawEnumerateEx function. (ANSI)
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Ddraw.dll 
req.header: ddraw.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Ddraw.lib 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: Windows 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Ddraw.dll
api_name:
 - DirectDrawEnumerateA
 - DirectDrawEnumerate
f1_keywords:
 - DirectDrawEnumerateA
 - ddraw/DirectDrawEnumerateA
 - DirectDrawEnumerate
 - ddraw/DirectDrawEnumerate
dev_langs:
 - c++
---

# DirectDrawEnumerateA function

## -description

This function is superseded by the <a href="/windows/desktop/api/ddraw/nf-ddraw-directdrawenumerateexa">DirectDrawEnumerateEx</a> function.

The <b>DirectDrawEnumerate</b> function enumerates the primary DirectDraw display device and a nondisplay device (such as a 3-D accelerator that has no 2-D capabilities), if one is installed. The NULL entry always identifies the primary display device shared with the GDI.

## -parameters

### -param lpCallback [in]

Address of a <a href="/windows/desktop/api/ddraw/nc-ddraw-lpddenumcallbacka">DDEnumCallback</a> function to be called with a description of each enumerated DirectDraw-enabled hardware abstraction layer (HAL).

### -param lpContext [in]

Address of an application-defined context to be passed to the enumeration callback function each time that it is called.

## -returns

If the function succeeds, the return value is <b>DD_OK</b>.

If it fails, the function returns <b>DDERR_INVALIDPARAMS</b>.

## -remarks

You must use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to access the <b>DirectDrawEnumerate</b> function.
