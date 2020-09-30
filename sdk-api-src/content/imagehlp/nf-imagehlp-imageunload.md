---
UID: NF:imagehlp.ImageUnload
title: ImageUnload function (imagehlp.h)
description: Deallocates resources from a previous call to the ImageLoad function.
helpviewer_keywords: ["ImageUnload","ImageUnload function","_win32_imageunload","base.imageunload","imagehlp/ImageUnload"]
old-location: base\imageunload.htm
tech.root: Debug
ms.assetid: 9cebd32f-11fe-4dfe-9579-b219d62c3e74
ms.date: 12/05/2018
ms.keywords: ImageUnload, ImageUnload function, _win32_imageunload, base.imageunload, imagehlp/ImageUnload
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
 - ImageUnload
 - imagehlp/ImageUnload
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
 - ImageUnload
---

# ImageUnload function


## -description

Deallocates resources from a previous call to the 
<a href="/windows/desktop/api/imagehlp/nf-imagehlp-imageload">ImageLoad</a> function.

## -parameters

### -param LoadedImage [in]

A pointer to a 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image">LOADED_IMAGE</a> structure that is returned from a call to the 
<a href="/windows/desktop/api/imagehlp/nf-imagehlp-imageload">ImageLoad</a> function.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.


<a href="/windows/desktop/api/imagehlp/nf-imagehlp-imageload">ImageLoad</a> and 
<b>ImageUnload</b> share internal data that can be corrupted if multiple consecutive calls to 
<b>ImageLoad</b> are performed. Therefore, make sure that you have called 
<b>ImageLoad</b> only once before calling 
<b>ImageUnload</b>.

## -remarks

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>



<a href="/windows/desktop/api/imagehlp/nf-imagehlp-imageload">ImageLoad</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image">LOADED_IMAGE</a>