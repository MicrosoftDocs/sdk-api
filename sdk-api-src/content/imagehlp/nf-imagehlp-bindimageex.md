---
UID: NF:imagehlp.BindImageEx
title: BindImageEx function (imagehlp.h)
description: Computes the virtual address of each function that is imported.
helpviewer_keywords: ["BIND_ALL_IMAGES","BIND_CACHE_IMPORT_DLLS","BIND_NO_BOUND_IMPORTS","BIND_NO_UPDATE","BindImageEx","BindImageEx function","_win32_bindimageex","base.bindimageex","imagehlp/BindImageEx"]
old-location: base\bindimageex.htm
tech.root: Debug
ms.assetid: 97edbe29-94e5-4d3c-b640-c92b7f01a159
ms.date: 12/05/2018
ms.keywords: BIND_ALL_IMAGES, BIND_CACHE_IMPORT_DLLS, BIND_NO_BOUND_IMPORTS, BIND_NO_UPDATE, BindImageEx, BindImageEx function, _win32_bindimageex, base.bindimageex, imagehlp/BindImageEx
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
 - BindImageEx
 - imagehlp/BindImageEx
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
 - BindImageEx
---

# BindImageEx function


## -description

Computes the virtual address of each function that is imported.

## -parameters

### -param Flags [in]

The bind options. This parameter can be a combination of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BIND_ALL_IMAGES"></a><a id="bind_all_images"></a><dl>
<dt><b>BIND_ALL_IMAGES</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Bind all images in the call tree for this file.

</td>
</tr>
<tr>
<td width="40%"><a id="BIND_CACHE_IMPORT_DLLS"></a><a id="bind_cache_import_dlls"></a><dl>
<dt><b>BIND_CACHE_IMPORT_DLLS</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Do not discard DLL information in the cache between calls. This improves performance when binding a large number of images.

</td>
</tr>
<tr>
<td width="40%"><a id="BIND_NO_BOUND_IMPORTS"></a><a id="bind_no_bound_imports"></a><dl>
<dt><b>BIND_NO_BOUND_IMPORTS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Do not generate a new import address table. 



							

</td>
</tr>
<tr>
<td width="40%"><a id="BIND_NO_UPDATE"></a><a id="bind_no_update"></a><dl>
<dt><b>BIND_NO_UPDATE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Do not make changes to the file.

</td>
</tr>
</table>

### -param ImageName [in]

The name of the file to be bound. This value can be a file name, a partial path, or a full path.

### -param DllPath [in]

The root of the search path to use if the file specified by the <i>ImageName</i> parameter cannot be opened.

### -param SymbolPath [in]

The root of the path to search for the file's corresponding symbol file.

### -param StatusRoutine [in]

A pointer to a status routine. The status routine is called during the progress of the image binding. For more information, see 
<a href="/windows/desktop/api/imagehlp/nc-imagehlp-pimagehlp_status_routine">StatusRoutine</a>.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The process of binding an image consists of computing the virtual address of each imported function. The computed virtual address is then saved in the importing image's Import Address Table (IAT). As a result, the image is loaded much faster, particularly if it uses many DLLs, because the system loader does not have to compute the address of each imported function.

If a corresponding symbol file can be located, its time stamp and checksum are updated.

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>



<a href="/windows/desktop/api/imagehlp/nc-imagehlp-pimagehlp_status_routine">StatusRoutine</a>