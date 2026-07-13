---
UID: NF:winddi.EngLoadModuleForWrite
title: EngLoadModuleForWrite function (winddi.h)
description: The EngLoadModuleForWrite function loads the specified executable module into system memory for writing.
helpviewer_keywords: ["EngLoadModuleForWrite","EngLoadModuleForWrite function [Display Devices]","display.engloadmoduleforwrite","gdifncs_ee01ce88-2028-4ba0-8800-b02d6534891b.xml","winddi/EngLoadModuleForWrite"]
old-location: display\engloadmoduleforwrite.htm
tech.root: display
ms.assetid: e5509142-624e-4c57-93b0-2579c6fb7089
ms.date: 12/05/2018
ms.keywords: EngLoadModuleForWrite, EngLoadModuleForWrite function [Display Devices], display.engloadmoduleforwrite, gdifncs_ee01ce88-2028-4ba0-8800-b02d6534891b.xml, winddi/EngLoadModuleForWrite
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
 - EngLoadModuleForWrite
 - winddi/EngLoadModuleForWrite
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
 - EngLoadModuleForWrite
---

# EngLoadModuleForWrite function


## -description

The <b>EngLoadModuleForWrite</b> function loads the specified executable module into system memory for writing.

## -parameters

### -param pwsz [in]

Pointer to a null-terminated string that contains the name of the file to be loaded.

### -param cjSizeOfModule [in]

Specifies the size, in bytes, of the module to be loaded.

## -returns

If <b>EngLoadModuleForWrite</b> succeeds, the return value is a handle to the module that was loaded. Otherwise, <b>NULL</b> is returned.

## -remarks

<b>EngLoadModuleForWrite</b> loads a data file into system memory with write permission. To access the loaded module, the driver should call <a href="/windows/desktop/api/winddi/nf-winddi-engmapmodule">EngMapModule</a> with the handle returned by this function.

<b>EndLoadModuleForWrite</b> loads the file into memory that is the same size as the file when <i>cjSizeOfModule</i> is zero. If <i>cjSizeOfModule</i> is greater than zero, GDI extends or truncates the file to be exactly <i>cjSizeOfModule</i> bytes in size before loading it. No assumptions should be made about the contents of memory that extend beyond the file when <i>cjSizeOfModule</i> is greater than the file's original size.

The file identified by <i>pwsz</i> must be located in the <i>%SystemRoot%\System32</i> directory or within a directory found in the directory hierarchy under <i>%SystemRoot%\System32</i>.

To load a module with read-only permissions, the driver should call <a href="/windows/desktop/api/winddi/nf-winddi-engloadmodule">EngLoadModule</a>. Drivers that need to load an image as executable code should call <a href="/windows/desktop/api/winddi/nf-winddi-engloadimage">EngLoadImage</a> instead of this function.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engfreemodule">EngFreeModule</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engloadimage">EngLoadImage</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engloadmodule">EngLoadModule</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engmapmodule">EngMapModule</a>