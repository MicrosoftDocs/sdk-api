---
UID: NF:ddraw.DirectDrawEnumerateExA
title: DirectDrawEnumerateExA function (ddraw.h)
description: Enumerates all DirectDraw devices that are installed on the computer. The NULL entry always identifies the primary display device that is shared with GDI. (ANSI)
helpviewer_keywords: ["DDENUM_ATTACHEDSECONDARYDEVICES", "DDENUM_DETACHEDSECONDARYDEVICES", "DDENUM_NONDISPLAYDEVICES", "DirectDrawEnumerateExA", "ddraw/DirectDrawEnumerateExA"]
old-location: directdraw\directdrawenumerateex.htm
tech.root: directdraw
ms.assetid: 38edfaaf-2c19-4836-b662-343312220032
ms.date: 12/05/2018
ms.keywords: DDENUM_ATTACHEDSECONDARYDEVICES, DDENUM_DETACHEDSECONDARYDEVICES, DDENUM_NONDISPLAYDEVICES, DirectDrawEnumerateEx, DirectDrawEnumerateEx function [DirectDraw], DirectDrawEnumerateExA, DirectDrawEnumerateExW, ddraw/DirectDrawEnumerateEx, ddraw/DirectDrawEnumerateExA, ddraw/DirectDrawEnumerateExW, directdraw.directdrawenumerateex
req.header: ddraw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DirectDrawEnumerateExW (Unicode) and DirectDrawEnumerateExA (ANSI)
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
 - DirectDrawEnumerateExA
 - ddraw/DirectDrawEnumerateExA
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
 - DirectDrawEnumerateEx
 - DirectDrawEnumerateExA
 - DirectDrawEnumerateExW
---

# DirectDrawEnumerateExA function


## -description

Enumerates all DirectDraw devices that are installed on the computer. The NULL entry always identifies the primary display device that is shared with GDI.

## -parameters

### -param lpCallback [in]

Address of a <a href="/windows/desktop/api/ddraw/nc-ddraw-lpddenumcallbackexa">DDEnumCallbackEx</a> function to be called with a description of each enumerated DirectDraw-enabled hardware abstraction layer (HAL).

### -param lpContext [in]

Address of an application-defined value to be passed to the enumeration callback function each time that it is called.

### -param dwFlags [in]

Flags that specify the enumeration scope. This parameter can be 0 or a combination of the following flags. If the value is 0, the function enumerates only the primary display device.



#### DDENUM_ATTACHEDSECONDARYDEVICES

The function enumerates the primary device and any display devices that are attached to the desktop.



#### DDENUM_DETACHEDSECONDARYDEVICES

The function enumerates the primary device and any display devices that are not attached to the desktop.



#### DDENUM_NONDISPLAYDEVICES

The function enumerates the primary device and any nondisplay devices, such as 3-D accelerators that have no 2-D capabilities.

## -returns

If the function succeeds, the return value is <b>DD_OK</b>.



If it fails, the function returns <b>DDERR_INVALIDPARAMS</b>.

## -remarks

On computers with multiple monitors, <b>DirectDrawEnumerateEx</b> enumerates multiple display devices. 



You must use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> to explicitly link to Ddraw.dll. To retrieve the address of the <b>DirectDrawEnumerateEx</b> function, call the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> Win32 function with the "DirectDrawEnumerateExA" (ANSI) or "DirectDrawEnumerateExW" (Unicode) process name strings.




> [!NOTE]
> The ddraw.h header defines DirectDrawEnumerateEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
