---
UID: NF:imagehlp.UnMapAndLoad
title: UnMapAndLoad function (imagehlp.h)
description: Deallocate all resources that are allocated by a previous call to the MapAndLoad function.
helpviewer_keywords: ["UnMapAndLoad","UnMapAndLoad function","_win32_unmapandload","base.unmapandload","imagehlp/UnMapAndLoad"]
old-location: base\unmapandload.htm
tech.root: Debug
ms.assetid: 63a39d2b-a3a1-4c91-be93-f9a681756293
ms.date: 12/05/2018
ms.keywords: UnMapAndLoad, UnMapAndLoad function, _win32_unmapandload, base.unmapandload, imagehlp/UnMapAndLoad
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
 - UnMapAndLoad
 - imagehlp/UnMapAndLoad
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
 - UnMapAndLoad
---

# UnMapAndLoad function


## -description

Deallocate all resources that are allocated by a previous call to the 
<a href="/windows/desktop/api/imagehlp/nf-imagehlp-mapandload">MapAndLoad</a> function.

## -parameters

### -param LoadedImage [in]

A pointer to a 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image">LOADED_IMAGE</a> structure. This structure is obtained through a call to the 
<a href="/windows/desktop/api/imagehlp/nf-imagehlp-mapandload">MapAndLoad</a> function.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>UnMapAndLoad</b> function must be used to deallocate all resources that are allocated by a previous call to 
<a href="/windows/desktop/api/imagehlp/nf-imagehlp-mapandload">MapAndLoad</a>. This function also writes a new checksum value into the image before the file is closed. This ensures that if a file is changed, it can be successfully loaded by the system loader.

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image">LOADED_IMAGE</a>



<a href="/windows/desktop/api/imagehlp/nf-imagehlp-mapandload">MapAndLoad</a>