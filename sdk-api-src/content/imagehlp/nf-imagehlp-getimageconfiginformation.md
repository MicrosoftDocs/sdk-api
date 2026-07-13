---
UID: NF:imagehlp.GetImageConfigInformation
title: GetImageConfigInformation function (imagehlp.h)
description: Locates and returns the load configuration data of an image.
helpviewer_keywords: ["GetImageConfigInformation","GetImageConfigInformation function","_win32_getimageconfiginformation","base.getimageconfiginformation","imagehlp/GetImageConfigInformation"]
old-location: base\getimageconfiginformation.htm
tech.root: Debug
ms.assetid: 5d9b6705-7e65-4a60-912e-8ffcff9d7921
ms.date: 12/05/2018
ms.keywords: GetImageConfigInformation, GetImageConfigInformation function, _win32_getimageconfiginformation, base.getimageconfiginformation, imagehlp/GetImageConfigInformation
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
 - GetImageConfigInformation
 - imagehlp/GetImageConfigInformation
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
 - GetImageConfigInformation
---

# GetImageConfigInformation function


## -description

Locates and returns the load configuration data of an image.

## -parameters

### -param LoadedImage [in]

A pointer to a 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image">LOADED_IMAGE</a> structure that is returned from a call to 
<a href="/windows/desktop/api/imagehlp/nf-imagehlp-mapandload">MapAndLoad</a> or <a href="/windows/desktop/api/imagehlp/nf-imagehlp-imageload">ImageLoad</a>.

### -param ImageConfigInformation [out]

A pointer to an IMAGE_LOAD_CONFIG_DIRECTORY structure that receives the configuration information.

If \_WIN64 is defined, then IMAGE_LOAD_CONFIG_DIRECTORY is defined as [IMAGE_LOAD_CONFIG_DIRECTORY64](/windows/desktop/api/winnt/ns-winnt-image_load_config_directory64). However, if \_WIN64 is not defined, then IMAGE_LOAD_CONFIG_DIRECTORY is defined as [IMAGE_LOAD_CONFIG_DIRECTORY32](/windows/desktop/api/winnt/ns-winnt-image_load_config_directory32).

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<a href="/windows/desktop/api/imagehlp/nf-imagehlp-setimageconfiginformation">SetImageConfigInformation</a> function locates and changes the load configuration data of an image.

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image">LOADED_IMAGE</a>
<a href="/windows/desktop/api/imagehlp/nf-imagehlp-setimageconfiginformation">SetImageConfigInformation</a>
