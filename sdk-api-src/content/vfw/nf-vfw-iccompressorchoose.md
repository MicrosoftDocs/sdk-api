---
UID: NF:vfw.ICCompressorChoose
title: ICCompressorChoose function (vfw.h)
description: The ICCompressorChoose function displays a dialog box in which a user can select a compressor. This function can display all registered compressors or list only the compressors that support a specific format.
helpviewer_keywords: ["ICCompressorChoose","ICCompressorChoose function [Windows Multimedia]","_win32_ICCompressorChoose","multimedia.iccompressorchoose","vfw/ICCompressorChoose"]
old-location: multimedia\iccompressorchoose.htm
tech.root: Multimedia
ms.assetid: 4a58df6a-9ac4-44bb-8c49-338bb60193fc
ms.date: 12/05/2018
ms.keywords: ICCompressorChoose, ICCompressorChoose function [Windows Multimedia], _win32_ICCompressorChoose, multimedia.iccompressorchoose, vfw/ICCompressorChoose
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
 - ICCompressorChoose
 - vfw/ICCompressorChoose
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
 - ICCompressorChoose
---

# ICCompressorChoose function


## -description

The <b>ICCompressorChoose</b> function displays a dialog box in which a user can select a compressor. This function can display all registered compressors or list only the compressors that support a specific format.

## -parameters

### -param hwnd

Handle to a parent window for the dialog box.

### -param uiFlags

Applicable flags. The following values are defined.

<table>
<tr>
<th>Value
                </th>
<th>Meaning
                </th>
</tr>
<tr>
<td>ICMF_CHOOSE_ALLCOMPRESSORS</td>
<td>All compressors should appear in the selection list. If this flag is not specified, only the compressors that can handle the input format appear in the selection list.</td>
</tr>
<tr>
<td>ICMF_CHOOSE_DATARATE</td>
<td>Displays a check box and edit box to enter the data rate for the movie.</td>
</tr>
<tr>
<td>ICMF_CHOOSE_KEYFRAME</td>
<td>Displays a check box and edit box to enter the frequency of key frames.</td>
</tr>
<tr>
<td>ICMF_CHOOSE_PREVIEW</td>
<td>Displays a button to expand the dialog box to include a preview window. The preview window shows how frames of your movie will appear when compressed with the current settings.</td>
</tr>
</table>

### -param pvIn

Uncompressed data input format. Only compressors that support the specified data input format are included in the compressor list. This parameter is optional.

### -param lpData

Pointer to an AVI stream interface to use in the preview window. You must specify a video stream. This parameter is optional.

### -param pc

Pointer to a <a href="/windows/desktop/api/vfw/ns-vfw-compvars">COMPVARS</a> structure. The information returned initializes the structure for use with other functions.

### -param lpszTitle

Pointer to a null-terminated string containing a title for the dialog box. This parameter is optional.

## -returns

Returns <b>TRUE</b> if the user chooses a compressor and presses OK. Returns <b>FALSE</b> on error or if the user presses CANCEL.

## -remarks

Before using this function, set the <b>cbSize</b> member of the <a href="/windows/desktop/api/vfw/ns-vfw-compvars">COMPVARS</a> structure to the size of the structure. Initialize the rest of the structure to zeros unless you want to specify some valid defaults for the dialog box. If specifying defaults, set the <i>dwFlags</i> member to ICMF_COMPVARS_VALID and initialize the other members of the structure. For more information about initializing the structure, see the <a href="/windows/desktop/api/vfw/nf-vfw-icseqcompressframestart">ICSeqCompressFrameStart</a> function and <b>COMPVARS</b>.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>