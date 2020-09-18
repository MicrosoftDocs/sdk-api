---
UID: NF:wingdi.DrawEscape
title: DrawEscape function (wingdi.h)
description: The DrawEscape function provides drawing capabilities of the specified video display that are not directly available through the graphics device interface (GDI).
helpviewer_keywords: ["DrawEscape","DrawEscape function [Windows GDI]","_win32_DrawEscape","gdi.drawescape","wingdi/DrawEscape"]
old-location: gdi\drawescape.htm
tech.root: gdi
ms.assetid: 306eec06-6d29-43bc-aff0-a267efa52ccd
ms.date: 12/05/2018
ms.keywords: DrawEscape, DrawEscape function [Windows GDI], _win32_DrawEscape, gdi.drawescape, wingdi/DrawEscape
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
 - DrawEscape
 - wingdi/DrawEscape
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
 - DrawEscape
---

# DrawEscape function


## -description

The <b>DrawEscape</b> function provides drawing capabilities of the specified video display that are not directly available through the graphics device interface (GDI).

## -parameters

### -param hdc [in]

A handle to the DC for the specified video display.

### -param iEscape [in]

The escape function to be performed.

### -param cjIn [in]

The number of bytes of data pointed to by the <i>lpszInData</i> parameter.

### -param lpIn [in]

A pointer to the input structure required for the specified escape.

## -returns

If the function is successful, the return value is greater than zero except for the QUERYESCSUPPORT draw escape, which checks for implementation only.

If the escape is not implemented, the return value is zero.

If an error occurred, the return value is less than zero.

## -remarks

When an application calls the <b>DrawEscape</b> function, the data identified by <i>cbInput</i> and <i>lpszInData</i> is passed directly to the specified display driver.

## -see-also

<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>