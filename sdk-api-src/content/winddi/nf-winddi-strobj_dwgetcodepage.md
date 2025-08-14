---
UID: NF:winddi.STROBJ_dwGetCodePage
title: STROBJ_dwGetCodePage function (winddi.h)
description: The STROBJ_dwGetCodePage function returns the code page associated with the specified STROBJ structure.
helpviewer_keywords: ["STROBJ_dwGetCodePage","STROBJ_dwGetCodePage function [Display Devices]","display.strobj_dwgetcodepage","gdifncs_e446480e-8516-4138-8121-1c9665fc22d9.xml","winddi/STROBJ_dwGetCodePage"]
old-location: display\strobj_dwgetcodepage.htm
tech.root: display
ms.assetid: b28e5854-1ac0-4b76-87a9-ec943228e2ed
ms.date: 12/05/2018
ms.keywords: STROBJ_dwGetCodePage, STROBJ_dwGetCodePage function [Display Devices], display.strobj_dwgetcodepage, gdifncs_e446480e-8516-4138-8121-1c9665fc22d9.xml, winddi/STROBJ_dwGetCodePage
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
 - STROBJ_dwGetCodePage
 - winddi/STROBJ_dwGetCodePage
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
 - STROBJ_dwGetCodePage
---

# STROBJ_dwGetCodePage function


## -description

The <b>STROBJ_dwGetCodePage</b> function returns the code page associated with the specified STROBJ structure.

## -parameters

### -param pstro

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-strobj">STROBJ</a> structure with which the code page is associated.

## -returns

<b>STROBJ_dwGetCodePage</b> returns a DWORD value that identifies the code page associated with the font used in the text output call at the Win32 API level.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-strobj">STROBJ</a>