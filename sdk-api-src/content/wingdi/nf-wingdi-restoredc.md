---
UID: NF:wingdi.RestoreDC
title: RestoreDC function (wingdi.h)
description: The RestoreDC function restores a device context (DC) to the specified state. The DC is restored by popping state information off a stack created by earlier calls to the SaveDC function.
helpviewer_keywords: ["RestoreDC","RestoreDC function [Windows GDI]","_win32_RestoreDC","gdi.restoredc","wingdi/RestoreDC"]
old-location: gdi\restoredc.htm
tech.root: gdi
ms.assetid: 7043edbb-b3ea-4946-a2ba-cae356b04d1d
ms.date: 12/05/2018
ms.keywords: RestoreDC, RestoreDC function [Windows GDI], _win32_RestoreDC, gdi.restoredc, wingdi/RestoreDC
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
 - RestoreDC
 - wingdi/RestoreDC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-DC-l1-2-0.dll
 - ext-ms-win-gdi-dc-l1-1-0.dll
 - ext-ms-win-gdi-dc-l1-2-1.dll
 - GDI32Full.dll
api_name:
 - RestoreDC
---

# RestoreDC function


## -description

The <b>RestoreDC</b> function restores a device context (DC) to the specified state. The DC is restored by popping state information off a stack created by earlier calls to the <a href="/windows/desktop/api/wingdi/nf-wingdi-savedc">SaveDC</a> function.

## -parameters

### -param hdc [in]

A handle to the DC.

### -param nSavedDC [in]

The saved state to be restored. If this parameter is positive, <i>nSavedDC</i> represents a specific instance of the state to be restored. If this parameter is negative, <i>nSavedDC</i> represents an instance relative to the current state. For example, -1 restores the most recently saved state.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

 Each DC maintains a stack of saved states. The <a href="/windows/desktop/api/wingdi/nf-wingdi-savedc">SaveDC</a> function pushes the current state of the DC onto its stack of saved states. That state can be restored only to the same DC from which it was created. After a state is restored, the saved state is destroyed and cannot be reused. Furthermore, any states saved after the restored state was created are also destroyed and cannot be used. In other words, the <b>RestoreDC</b> function pops the restored state (and any subsequent states) from the state information stack.

## -see-also

<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-savedc">SaveDC</a>