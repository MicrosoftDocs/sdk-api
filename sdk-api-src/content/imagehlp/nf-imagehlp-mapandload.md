---
UID: NF:imagehlp.MapAndLoad
title: MapAndLoad function (imagehlp.h)
description: Maps an image and preloads data from the mapped file.
helpviewer_keywords: ["MapAndLoad","MapAndLoad function","_win32_mapandload","base.mapandload","imagehlp/MapAndLoad"]
old-location: base\mapandload.htm
tech.root: Debug
ms.assetid: 42d5ea46-4b89-4d93-b9a9-18c2855df193
ms.date: 12/05/2018
ms.keywords: MapAndLoad, MapAndLoad function, _win32_mapandload, base.mapandload, imagehlp/MapAndLoad
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
 - MapAndLoad
 - imagehlp/MapAndLoad
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
 - MapAndLoad
---

# MapAndLoad function


## -description

Maps an image and preloads data from the mapped file.

## -parameters

### -param ImageName [in]

The file name of the image (executable file or DLL) that is loaded.

### -param DllPath [in]

The path used to locate the image if the name provided cannot be found. If this parameter is <b>NULL</b>, then the search path rules set using the 
<a href="/windows/desktop/api/processenv/nf-processenv-searchpathw">SearchPath</a> function apply.

### -param LoadedImage [out]

A pointer to a 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image">LOADED_IMAGE</a> structure that receives information about the image after it is loaded.

### -param DotDll [in]

The default extension to be used if the image name does not contain a file name extension. If the value is <b>TRUE</b>, a .DLL extension is used. If the value is <b>FALSE</b>, then an .EXE extension is used.

### -param ReadOnly [in]

The access mode. If this value is <b>TRUE</b>, the file is mapped for read-access only. If the value is <b>FALSE</b>, the file is mapped for read and write access.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>MapAndLoad</b> function maps an image and preloads data from the mapped file. The corresponding function, 
<a href="/windows/desktop/api/imagehlp/nf-imagehlp-unmapandload">UnMapAndLoad</a>, must be used to deallocate all resources that are allocated by the 
<b>MapAndLoad</b> function.
			

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image">LOADED_IMAGE</a>



<a href="/windows/desktop/api/imagehlp/nf-imagehlp-unmapandload">UnMapAndLoad</a>