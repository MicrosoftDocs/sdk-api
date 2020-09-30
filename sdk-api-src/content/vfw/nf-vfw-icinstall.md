---
UID: NF:vfw.ICInstall
title: ICInstall function (vfw.h)
description: The ICInstall function installs a new compressor or decompressor.
helpviewer_keywords: ["ICInstall","ICInstall function [Windows Multimedia]","_win32_ICInstall","multimedia.icinstall","vfw/ICInstall"]
old-location: multimedia\icinstall.htm
tech.root: Multimedia
ms.assetid: 23bbc186-3ef9-479a-94f9-a97269cf6dbc
ms.date: 12/05/2018
ms.keywords: ICInstall, ICInstall function [Windows Multimedia], _win32_ICInstall, multimedia.icinstall, vfw/ICInstall
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICInstall
 - vfw/ICInstall
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - ICInstall
---

# ICInstall function


## -description

The <b>ICInstall</b> function installs a new compressor or decompressor.

## -parameters

### -param fccType

Four-character code indicating the type of data used by the compressor or decompressor. Specify "VIDC" for a video compressor or decompressor.

### -param fccHandler

Four-character code identifying a specific compressor or decompressor.

### -param lParam

Pointer to a null-terminated string containing the name of the compressor or decompressor, or the address of a function used for compression or decompression. The contents of this parameter are defined by the flags set for <i>wFlags</i>.

### -param szDesc

Reserved; do not use.

### -param wFlags

Flags defining the contents of <i>lParam</i>. The following values are defined.

<table>
<tr>
<th>Value
                </th>
<th>Meaning
                </th>
</tr>
<tr>
<td>ICINSTALL_DRIVER</td>
<td>The <i>lParam</i> parameter contains the address of a null-terminated string that names the compressor to install.</td>
</tr>
<tr>
<td>ICINSTALL_FUNCTION</td>
<td>The <i>lParam</i> parameter contains the address of a compressor function. This function should be structured like the <a href="/previous-versions/dd797918(v=vs.85)">DriverProc</a> entry point function used by compressors.</td>
</tr>
</table>

## -returns

Returns ICERR_OK if successful or an error otherwise.

## -remarks

Applications must open an installed compressor or decompressor before using it.

If your application installs a function as a compressor or decompressor, it should remove the function with the <a href="/windows/desktop/api/vfw/nf-vfw-icremove">ICRemove</a> function before it terminates. This prevents other applications from trying to access the function when it is not available.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>