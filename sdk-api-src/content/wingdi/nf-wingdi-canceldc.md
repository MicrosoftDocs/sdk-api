---
UID: NF:wingdi.CancelDC
title: CancelDC function (wingdi.h)
description: The CancelDC function cancels any pending operation on the specified device context (DC).
helpviewer_keywords: ["CancelDC","CancelDC function [Windows GDI]","_win32_CancelDC","gdi.canceldc","wingdi/CancelDC"]
old-location: gdi\canceldc.htm
tech.root: gdi
ms.assetid: 1dcb3dfe-0ab0-4bf5-ac2f-7a9c11712eef
ms.date: 12/05/2018
ms.keywords: CancelDC, CancelDC function [Windows GDI], _win32_CancelDC, gdi.canceldc, wingdi/CancelDC
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CancelDC
 - wingdi/CancelDC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - CancelDC
---

# CancelDC function


## -description

The <b>CancelDC</b> function cancels any pending operation on the specified device context (DC).

## -parameters

### -param hdc [in]

A handle to the DC.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The <b>CancelDC</b> function is used by multithreaded applications to cancel lengthy drawing operations. If thread A initiates a lengthy drawing operation, thread B may cancel that operation by calling this function.

If an operation is canceled, the affected thread returns an error and the result of its drawing operation is undefined. The results are also undefined if no drawing operation was in progress when the function was called.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread">CreateThread</a>



<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthread">GetCurrentThread</a>