---
UID: NF:winddi.EngMapModule
title: EngMapModule function (winddi.h)
description: The EngMapModule function returns the address and size of a file that was loaded by EngLoadModule, EngLoadModuleForWrite, EngLoadImage, or EngMapFile.
helpviewer_keywords: ["EngMapModule","EngMapModule function [Display Devices]","display.engmapmodule","gdifncs_c3731e1a-e853-403b-958b-370494e79ae7.xml","winddi/EngMapModule"]
old-location: display\engmapmodule.htm
tech.root: display
ms.assetid: f8bd9b2c-11a3-454f-a4ce-cbda28115564
ms.date: 12/05/2018
ms.keywords: EngMapModule, EngMapModule function [Display Devices], display.engmapmodule, gdifncs_c3731e1a-e853-403b-958b-370494e79ae7.xml, winddi/EngMapModule
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
 - EngMapModule
 - winddi/EngMapModule
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
 - EngMapModule
---

# EngMapModule function


## -description

The <b>EngMapModule</b> function returns the address and size of a file that was loaded by <a href="/windows/desktop/api/winddi/nf-winddi-engloadmodule">EngLoadModule</a>, <a href="/windows/desktop/api/winddi/nf-winddi-engloadmoduleforwrite">EngLoadModuleForWrite</a>, <a href="/windows/desktop/api/winddi/nf-winddi-engloadimage">EngLoadImage</a>, or <a href="/windows/desktop/api/winddi/nf-winddi-engmapfile">EngMapFile</a>.

## -parameters

### -param h [in]

Handle to the file to be memory-mapped.

### -param pSize [in]

Pointer to a memory location that receives the size, in bytes, of the memory-mapped file.

## -returns

<b>EngMapModule</b> returns a pointer to the view of the file identified by <i>h</i>.

## -remarks

A driver can open and read a file using <a href="/windows/desktop/api/winddi/nf-winddi-engloadmodule">EngLoadModule</a> and <b>EngMapModule</b>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engfreemodule">EngFreeModule</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engloadimage">EngLoadImage</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engloadmodule">EngLoadModule</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engloadmoduleforwrite">EngLoadModuleForWrite</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engmapfile">EngMapFile</a>