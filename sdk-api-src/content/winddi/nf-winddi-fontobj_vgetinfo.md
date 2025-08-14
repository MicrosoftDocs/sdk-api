---
UID: NF:winddi.FONTOBJ_vGetInfo
title: FONTOBJ_vGetInfo function (winddi.h)
description: The FONTOBJ_vGetInfo function retrieves information about an associated font.
helpviewer_keywords: ["FONTOBJ_vGetInfo","FONTOBJ_vGetInfo function [Display Devices]","display.fontobj_vgetinfo","gdifncs_0b07bb13-32b4-404c-824f-02f2b5659295.xml","winddi/FONTOBJ_vGetInfo"]
old-location: display\fontobj_vgetinfo.htm
tech.root: display
ms.assetid: 4b952bdc-a496-4ded-9390-9f4b470f3a6c
ms.date: 12/05/2018
ms.keywords: FONTOBJ_vGetInfo, FONTOBJ_vGetInfo function [Display Devices], display.fontobj_vgetinfo, gdifncs_0b07bb13-32b4-404c-824f-02f2b5659295.xml, winddi/FONTOBJ_vGetInfo
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
 - FONTOBJ_vGetInfo
 - winddi/FONTOBJ_vGetInfo
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
 - FONTOBJ_vGetInfo
---

# FONTOBJ_vGetInfo function


## -description

The <b>FONTOBJ_vGetInfo</b> function retrieves information about an associated font.

## -parameters

### -param pfo

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a> structure to be queried.

### -param cjSize [in]

Specifies the size in bytes of the buffer pointed to by <i>pfi</i>.

### -param pfi

Pointer to a buffer previously allocated by the driver. GDI writes a <a href="/windows/desktop/api/winddi/ns-winddi-fontinfo">FONTINFO</a> structure to this buffer.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-fontinfo">FONTINFO</a>



<a href="/windows/desktop/api/winddi/ns-winddi-fontobj">FONTOBJ</a>