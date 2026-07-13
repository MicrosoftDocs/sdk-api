---
UID: NF:wingdi.GetDCOrgEx
title: GetDCOrgEx function (wingdi.h)
description: The GetDCOrgEx function retrieves the final translation origin for a specified device context (DC).
helpviewer_keywords: ["GetDCOrgEx","GetDCOrgEx function [Windows GDI]","_win32_GetDCOrgEx","gdi.getdcorgex","wingdi/GetDCOrgEx"]
old-location: gdi\getdcorgex.htm
tech.root: gdi
ms.assetid: 795c6a69-7146-4d1a-abf9-ce1d740ca946
ms.date: 12/05/2018
ms.keywords: GetDCOrgEx, GetDCOrgEx function [Windows GDI], _win32_GetDCOrgEx, gdi.getdcorgex, wingdi/GetDCOrgEx
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
 - GetDCOrgEx
 - wingdi/GetDCOrgEx
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
 - GetDCOrgEx
---

# GetDCOrgEx function


## -description

The <b>GetDCOrgEx</b> function retrieves the final translation origin for a specified device context (DC). The final translation origin specifies an offset that the system uses to translate device coordinates into client coordinates (for coordinates in an application's window).

## -parameters

### -param hdc [in]

A handle to the DC whose final translation origin is to be retrieved.

### -param lppt [out]

A pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that receives the final translation origin, in device coordinates.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The final translation origin is relative to the physical origin of the screen.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createica">CreateIC</a>



<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>