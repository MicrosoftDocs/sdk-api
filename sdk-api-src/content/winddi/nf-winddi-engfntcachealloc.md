---
UID: NF:winddi.EngFntCacheAlloc
title: EngFntCacheAlloc function (winddi.h)
author: windows-sdk-content
description: The EngFntCacheAlloc function allocates storage for a font that is to be stored in cached memory.
old-location: display\engfntcachealloc.htm
tech.root: display
ms.assetid: fd0765e0-decd-46fb-872e-4c750713abe6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EngFntCacheAlloc, EngFntCacheAlloc function [Display Devices], display.engfntcachealloc, gdifncs_c2f9bace-a686-42e3-b72c-bd6d109786a6.xml, winddi/EngFntCacheAlloc
ms.topic: function
f1_keywords: 
 - "winddi/EngFntCacheAlloc"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngFntCacheAlloc
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EngFntCacheAlloc function


## -description


The <b>EngFntCacheAlloc</b> function allocates storage for a font that is to be stored in cached memory.


## -parameters




### -param FastCheckSum [in]

Specifies the checksum for the font. 


### -param ulSize [in]

Specifies the number of bytes of storage to allocate.


## -returns



On success, this function returns the address of the cache of font data. Otherwise, it returns <b>NULL</b>.




## -remarks



When the font driver calls this function, the font engine allocates memory in which the font driver stores font data. 

The font engine calls the font driver's <a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-drvloadfontfile">DrvLoadFontFile</a> entry point when a font file is first loaded. It is in this call that the font driver receives a value for <i>FastCheckSum</i>, which it subsequently uses when it calls this function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-drvloadfontfile">DrvLoadFontFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-engfntcachefault">EngFntCacheFault</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-engfntcachelookup">EngFntCacheLookUp</a>
 

 

