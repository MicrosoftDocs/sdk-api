---
UID: NF:winddi.EngLoadImage
title: EngLoadImage macro (winddi.h)
description: The EngLoadImage function loads the specified executable image into kernel-mode memory.
helpviewer_keywords: ["EngLoadImage","EngLoadImage function [Display Devices]","display.engloadimage","gdifncs_8fb20a2d-c7ae-4d15-af65-219b44289130.xml","winddi/EngLoadImage"]
old-location: display\engloadimage.htm
tech.root: display
ms.assetid: 03b1835a-5c4e-4f38-93b1-e557a2975be7
ms.date: 12/05/2018
ms.keywords: EngLoadImage, EngLoadImage function [Display Devices], display.engloadimage, gdifncs_8fb20a2d-c7ae-4d15-af65-219b44289130.xml, winddi/EngLoadImage
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
 - EngLoadImage
 - winddi/EngLoadImage
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
 - EngLoadImage
---

# EngLoadImage macro


## -description

The <b>EngLoadImage</b> function loads the specified executable image into kernel-mode memory.

## -parameters

### -param filename [in]

Pointer to a null-terminated string that names the file containing the executable image to be loaded.

## -remarks

A driver can use <b>EngLoadImage</b> to map an executable image into kernel-mode memory. For example, a printer driver can call <b>EngLoadImage</b> to load a minidriver.

<b>EngLoadImage</b> requires that the image file to be loaded have a <i>.dll</i> suffix. The driver must include this suffix in the <i>pwszDriver</i> string.

To execute a section of code within the loaded image, the driver should obtain the function address from <a href="/windows/desktop/api/winddi/nf-winddi-engfindimageprocaddress">EngFindImageProcAddress</a>.

The file identified by <i>pwszDriver</i> must be located in the <i>%SystemRoot%\System32</i> directory or within a directory found in the directory hierarchy under <i>%SystemRoot%\System32</i>.

Drivers that need to load a module as data only should call <a href="/windows/desktop/api/winddi/nf-winddi-engloadmodule">EngLoadModule</a> or <a href="/windows/desktop/api/winddi/nf-winddi-engloadmoduleforwrite">EngLoadModuleForWrite</a> instead of this function.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engloadmodule">EngLoadModule</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engloadmoduleforwrite">EngLoadModuleForWrite</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engunloadimage">EngUnloadImage</a>