---
UID: NF:ddraw.DirectDrawEnumerateW
title: DirectDrawEnumerateW function (ddraw.h)
description: This function is superseded by the DirectDrawEnumerateEx function. (Unicode)
helpviewer_keywords: ["DirectDrawEnumerate", "DirectDrawEnumerate function [DirectDraw]", "DirectDrawEnumerateW", "ddraw/DirectDrawEnumerate", "ddraw/DirectDrawEnumerateW", "directdraw.directdrawenumerate"]
old-location: directdraw\directdrawenumerate.htm
tech.root: directdraw
ms.assetid: 1f994adb-79ff-4cc1-8769-0faeed893503
ms.date: 12/05/2018
ms.keywords: DirectDrawEnumerate, DirectDrawEnumerate function [DirectDraw], DirectDrawEnumerateW, ddraw/DirectDrawEnumerate, ddraw/DirectDrawEnumerateW, directdraw.directdrawenumerate
req.header: ddraw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DirectDrawEnumerateW (Unicode) and DirectDrawEnumerate (ANSI)
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
 - DirectDrawEnumerateW
 - ddraw/DirectDrawEnumerateW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ddraw.dll
api_name:
 - DirectDrawEnumerate
 - DirectDrawEnumerate
 - DirectDrawEnumerateW
---

# DirectDrawEnumerateW function


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
