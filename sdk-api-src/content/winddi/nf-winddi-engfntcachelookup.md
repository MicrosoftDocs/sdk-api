---
UID: NF:winddi.EngFntCacheLookUp
title: EngFntCacheLookUp function (winddi.h)
description: The EngFntCacheLookUp function retrieves the address of cached font file data.
helpviewer_keywords: ["EngFntCacheLookUp","EngFntCacheLookUp function [Display Devices]","display.engfntcachelookup","gdifncs_2fee1e8e-2cb5-4088-b0aa-f697689fe56f.xml","winddi/EngFntCacheLookUp"]
old-location: display\engfntcachelookup.htm
tech.root: display
ms.assetid: daf93826-fdcb-4c9d-ade6-ad4f0ef40ff5
ms.date: 12/05/2018
ms.keywords: EngFntCacheLookUp, EngFntCacheLookUp function [Display Devices], display.engfntcachelookup, gdifncs_2fee1e8e-2cb5-4088-b0aa-f697689fe56f.xml, winddi/EngFntCacheLookUp
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
 - EngFntCacheLookUp
 - winddi/EngFntCacheLookUp
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
 - EngFntCacheLookUp
---

# EngFntCacheLookUp function


## -description

The <b>EngFntCacheLookUp</b> function retrieves the address of cached font file data.

## -parameters

### -param FastCheckSum [in]

Specifies the checksum for the font.

### -param pulSize [out]

Pointer to a memory location that receives the size, in bytes, of the data.

## -returns

On success, this function returns a pointer to the cached data. Otherwise, it returns <b>NULL</b>.

## -remarks

The font engine calls the font driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvloadfontfile">DrvLoadFontFile</a> entry point when a font file is first loaded. It is in this call that the font driver receives a value for <i>FastCheckSum</i>, which it subsequently uses when it calls this function.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvloadfontfile">DrvLoadFontFile</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engfntcachealloc">EngFntCacheAlloc</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engfntcachefault">EngFntCacheFault</a>