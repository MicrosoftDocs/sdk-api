---
UID: NF:imagehlp.SetImageConfigInformation
title: SetImageConfigInformation function (imagehlp.h)
description: Locates and changes the load configuration data of an image.
helpviewer_keywords: ["SetImageConfigInformation","SetImageConfigInformation function","_win32_setimageconfiginformation","base.setimageconfiginformation","imagehlp/SetImageConfigInformation"]
old-location: base\setimageconfiginformation.htm
tech.root: Debug
ms.assetid: 396af0c0-2fb1-418b-bc2b-9e9eb63174bc
ms.date: 12/05/2018
ms.keywords: SetImageConfigInformation, SetImageConfigInformation function, _win32_setimageconfiginformation, base.setimageconfiginformation, imagehlp/SetImageConfigInformation
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
 - SetImageConfigInformation
 - imagehlp/SetImageConfigInformation
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
 - SetImageConfigInformation
---

# SetImageConfigInformation function


## -description

Locates and changes the load configuration data of an image.

## -parameters

### -param LoadedImage [in]

A pointer to a 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image">LOADED_IMAGE</a> structure that is returned from a call to 
<a href="/windows/desktop/api/imagehlp/nf-imagehlp-mapandload">MapAndLoad</a> or <b>LoadImage</b>.

### -param ImageConfigInformation [in]

A pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-image_load_config_directory32">IMAGE_LOAD_CONFIG_DIRECTORY64</a> structure.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>SetImageConfigInformation</b> function locates and returns the load configuration data of an image.

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/api/imagehlp/nf-imagehlp-getimageconfiginformation">GetImageConfigInformation</a>



<a href="/windows/desktop/api/winnt/ns-winnt-image_load_config_directory32">IMAGE_LOAD_CONFIG_DIRECTORY64</a>



<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image">LOADED_IMAGE</a>