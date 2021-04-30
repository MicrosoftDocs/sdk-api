---
UID: NF:imagehlp.ImageLoad
title: ImageLoad function (imagehlp.h)
description: Maintains a list of loaded DLLs.
helpviewer_keywords: ["ImageLoad","ImageLoad function","_win32_imageload","base.imageload","imagehlp/ImageLoad"]
old-location: base\imageload.htm
tech.root: Debug
ms.assetid: e88e6417-a805-43c2-9f47-5180228cf175
ms.date: 12/05/2018
ms.keywords: ImageLoad, ImageLoad function, _win32_imageload, base.imageload, imagehlp/ImageLoad
req.header: imagehlp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Imagehlp.lib
req.dll: Imagehlp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImageLoad
 - imagehlp/ImageLoad
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Imagehlp.dll
api_name:
 - ImageLoad
---

# ImageLoad function


## -description

Maintains a list of loaded DLLs.

## -parameters

### -param DllName [in]

The name of the image.

### -param DllPath [in]

The path used to locate the image if the name provided cannot be found. If <b>NULL</b> is used, then the search path rules set forth in the 
<a href="/windows/desktop/api/processenv/nf-processenv-searchpathw">SearchPath</a> function apply.

## -returns

If the function succeeds, the return value is a pointer to a 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image">LOADED_IMAGE</a> structure.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>ImageLoad</b> function is used to maintain a list of loaded DLLs. If the image has already been loaded, the prior 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image">LOADED_IMAGE</a> is returned. Otherwise, the new image is added to the list.

The 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image">LOADED_IMAGE</a> structure must be deallocated by the 
<a href="/windows/desktop/api/imagehlp/nf-imagehlp-imageunload">ImageUnload</a> function.

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>



<a href="/windows/desktop/api/imagehlp/nf-imagehlp-imageunload">ImageUnload</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image">LOADED_IMAGE</a>