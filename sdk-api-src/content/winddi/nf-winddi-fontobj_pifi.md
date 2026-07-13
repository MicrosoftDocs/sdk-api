---
UID: NF:winddi.FONTOBJ_pifi
title: FONTOBJ_pifi function (winddi.h)
description: The FONTOBJ_pifi function retrieves the pointer to the IFIMETRICS structure associated with a specified font.
helpviewer_keywords: ["FONTOBJ_pifi","FONTOBJ_pifi function [Display Devices]","display.fontobj_pifi","gdifncs_702d11ac-850f-4e4d-aefa-1ccf404edb56.xml","winddi/FONTOBJ_pifi"]
old-location: display\fontobj_pifi.htm
tech.root: display
ms.assetid: 797341c8-7346-477a-9c7c-b6abbeaac4b2
ms.date: 12/05/2018
ms.keywords: FONTOBJ_pifi, FONTOBJ_pifi function [Display Devices], display.fontobj_pifi, gdifncs_702d11ac-850f-4e4d-aefa-1ccf404edb56.xml, winddi/FONTOBJ_pifi
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FONTOBJ_pifi
 - winddi/FONTOBJ_pifi
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - FONTOBJ_pifi
---

# FONTOBJ_pifi function


## -description

The <b>FONTOBJ_pifi</b> function retrieves the pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-ifimetrics">IFIMETRICS</a> structure associated with a specified font.

## -parameters

### -param pfo

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a> structure for which the associated IFIMETRICS structure is to be retrieved.

## -returns

The return value is a pointer to the IFIMETRICS structure associated with the specified font if the function is successful. Otherwise, it is <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-ifimetrics">IFIMETRICS</a>