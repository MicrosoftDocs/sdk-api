---
UID: NF:winddi.EngLoadModule
title: EngLoadModule function (winddi.h)
description: The EngLoadModule function loads the specified data module into system memory for reading.
helpviewer_keywords: ["EngLoadModule","EngLoadModule function [Display Devices]","display.engloadmodule","gdifncs_43b05b8f-ecc9-4097-81d3-39716dabaf2f.xml","winddi/EngLoadModule"]
old-location: display\engloadmodule.htm
tech.root: display
ms.assetid: 0327d3f0-f9ee-4715-aa0e-ad1d0544a1ff
ms.date: 12/05/2018
ms.keywords: EngLoadModule, EngLoadModule function [Display Devices], display.engloadmodule, gdifncs_43b05b8f-ecc9-4097-81d3-39716dabaf2f.xml, winddi/EngLoadModule
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
 - EngLoadModule
 - winddi/EngLoadModule
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - EngLoadModule
---

# EngLoadModule function


## -description

The <b>EngLoadModule</b> function loads the specified data module into system memory for reading.

## -parameters

### -param pwsz [in]

Pointer to a null-terminated string that contains the name of the data file to be loaded.

## -returns

If <b>EngLoadModule</b> succeeds, the return value is a handle to the module that was loaded. Otherwise, the return value is <b>NULL</b>.

## -remarks

<b>EngLoadModule</b> loads a data file into system memory with read-only permission. To access the loaded module, the driver should call <a href="/windows/desktop/api/winddi/nf-winddi-engmapmodule">EngMapModule</a> with the handle returned by this function.

The file identified by <i>pwsz</i> must be located in the <i>%SystemRoot%\System32</i> directory or within a directory found in the directory hierarchy under <i>%SystemRoot%\System32</i>.

To load a writable module, the driver should call <a href="/windows/desktop/api/winddi/nf-winddi-engloadmoduleforwrite">EngLoadModuleForWrite</a>. Drivers that need to load an image as executable code should call <a href="/windows/desktop/api/winddi/nf-winddi-engloadimage">EngLoadImage</a> instead of this function.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engfreemodule">EngFreeModule</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engloadmoduleforwrite">EngLoadModuleForWrite</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engmapmodule">EngMapModule</a>