---
UID: NF:imagehlp.BindImage
title: BindImage function (imagehlp.h)
description: Computes the virtual address of each imported function.
helpviewer_keywords: ["BindImage","BindImage function","_win32_bindimage","base.bindimage","imagehlp/BindImage"]
old-location: base\bindimage.htm
tech.root: Debug
ms.assetid: d586bf3a-c911-44a3-bf92-7de35009f742
ms.date: 12/05/2018
ms.keywords: BindImage, BindImage function, _win32_bindimage, base.bindimage, imagehlp/BindImage
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
 - BindImage
 - imagehlp/BindImage
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
 - BindImage
---

# BindImage function


## -description

Computes the virtual address of each imported function.

This function has been superseded by the 
<a href="/windows/desktop/api/imagehlp/nf-imagehlp-bindimageex">BindImageEx</a> function. Use 
<b>BindImageEx</b> to provide a status routine or flags to control the image binding.

## -parameters

### -param ImageName [in]

The name of the file to be bound. This value can be a file name, a partial path, or a full path.

### -param DllPath [in]

The root of the search path to use if the file specified by the <i>ImageName</i> parameter cannot be opened.

### -param SymbolPath [in]

The root of the path to search for the file's corresponding symbol file.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A call to 
<b>BindImage</b> is equivalent to the following call: <code>BindImageEx( 0, ImageName, DllPath, SymbolPath, NULL );</code>

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/api/imagehlp/nf-imagehlp-bindimageex">BindImageEx</a>



<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>