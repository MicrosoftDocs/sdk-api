---
UID: NF:winddi.EngFntCacheFault
title: EngFntCacheFault function (winddi.h)
description: The EngFntCacheFault function reports an error to the font engine if the font driver encountered an error reading from or writing to a font data cache.
helpviewer_keywords: ["EngFntCacheFault","EngFntCacheFault function [Display Devices]","display.engfntcachefault","gdifncs_f6395707-6ff6-4396-b280-77d4256db07b.xml","winddi/EngFntCacheFault"]
old-location: display\engfntcachefault.htm
tech.root: display
ms.assetid: 27a44779-64df-4a3f-b8b8-9e0417010969
ms.date: 12/05/2018
ms.keywords: EngFntCacheFault, EngFntCacheFault function [Display Devices], display.engfntcachefault, gdifncs_f6395707-6ff6-4396-b280-77d4256db07b.xml, winddi/EngFntCacheFault
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: This function is available in Windows XP and later.
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
 - EngFntCacheFault
 - winddi/EngFntCacheFault
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
 - EngFntCacheFault
---

# EngFntCacheFault function


## -description

The <b>EngFntCacheFault</b> function reports an error to the font engine if the font driver encountered an error reading from or writing to a font data cache.

## -parameters

### -param ulFastCheckSum [in]

Specifies the checksum for the font.

### -param iFaultMode [in]

Specifies the type of error that occurred. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
ENG_FNT_CACHE_READ_FAULT

</td>
<td>
An error occurred during retrieval.

</td>
</tr>
<tr>
<td>
ENG_FNT_CACHE_WRITE_FAULT

</td>
<td>
An error occurred during storage.

</td>
</tr>
</table>

## -returns

None

## -remarks

If an error occurs while the font driver was reading from or writing to the font data cache, it should report the error to the font engine by a call to this function.

The font engine calls the font driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvloadfontfile">DrvLoadFontFile</a> entry point when a font file is first loaded. It is in this call that the font driver receives a value for <i>ulFastCheckSum</i>, which it subsequently uses when it calls this function.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvloadfontfile">DrvLoadFontFile</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engfntcachealloc">EngFntCacheAlloc</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engfntcachelookup">EngFntCacheLookUp</a>