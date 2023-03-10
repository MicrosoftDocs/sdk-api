---
UID: NF:imagehlp.GetImageUnusedHeaderBytes
title: GetImageUnusedHeaderBytes function (imagehlp.h)
description: Retrieves the offset and size of the part of the PE header that is currently unused.
helpviewer_keywords: ["GetImageUnusedHeaderBytes","GetImageUnusedHeaderBytes function","_win32_getimageunusedheaderbytes","base.getimageunusedheaderbytes","imagehlp/GetImageUnusedHeaderBytes"]
old-location: base\getimageunusedheaderbytes.htm
tech.root: Debug
ms.assetid: 4ad9c833-693b-4c19-b397-f97f166efadc
ms.date: 12/05/2018
ms.keywords: GetImageUnusedHeaderBytes, GetImageUnusedHeaderBytes function, _win32_getimageunusedheaderbytes, base.getimageunusedheaderbytes, imagehlp/GetImageUnusedHeaderBytes
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
 - GetImageUnusedHeaderBytes
 - imagehlp/GetImageUnusedHeaderBytes
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
 - GetImageUnusedHeaderBytes
---

# GetImageUnusedHeaderBytes function


## -description

Retrieves the offset and size of the part of the PE header that is currently unused.

## -parameters

### -param LoadedImage [in]

A pointer to a 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image">LOADED_IMAGE</a> structure that is returned from a call to 
<a href="/windows/desktop/api/imagehlp/nf-imagehlp-mapandload">MapAndLoad</a> or <a href="/windows/desktop/api/imagehlp/nf-imagehlp-imageload">ImageLoad</a>.

### -param SizeUnusedHeaderBytes [out]

A pointer to a variable to receive the size, in bytes, of the part of the image's header which is unused.

## -returns

If the function succeeds, the return value is the offset from the base address of the first unused header byte.

If the function fails, the return value is zero. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image">LOADED_IMAGE</a>