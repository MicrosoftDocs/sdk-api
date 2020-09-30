---
UID: NF:vfw.AVISaveOptions
title: AVISaveOptions function (vfw.h)
description: The AVISaveOptions function retrieves the save options for a file and returns them in a buffer.
helpviewer_keywords: ["AVISaveOptions","AVISaveOptions function [Windows Multimedia]","_win32_AVISaveOptions","multimedia.avisaveoptions","vfw/AVISaveOptions"]
old-location: multimedia\avisaveoptions.htm
tech.root: Multimedia
ms.assetid: 6141272f-a815-4ba8-bc6b-41751d6e0104
ms.date: 12/05/2018
ms.keywords: AVISaveOptions, AVISaveOptions function [Windows Multimedia], _win32_AVISaveOptions, multimedia.avisaveoptions, vfw/AVISaveOptions
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
req.dll: Avifil32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AVISaveOptions
 - vfw/AVISaveOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avifil32.dll
api_name:
 - AVISaveOptions
---

# AVISaveOptions function


## -description

The <b>AVISaveOptions</b> function retrieves the save options for a file and returns them in a buffer.

## -parameters

### -param hwnd

Handle to the parent window for the Compression Options dialog box.

### -param uiFlags

Flags for displaying the Compression Options dialog box. The following flags are defined.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>ICMF_CHOOSE_KEYFRAME</td>
<td>Displays a Key Frame Every dialog box for the video options. This is the same flag used in the <a href="/windows/desktop/api/vfw/nf-vfw-iccompressorchoose">ICCompressorChoose</a> function.</td>
</tr>
<tr>
<td>ICMF_CHOOSE_DATARATE</td>
<td>Displays a Data Rate dialog box for the video options. This is the same flag used in <a href="/windows/desktop/api/vfw/nf-vfw-iccompressorchoose">ICCompressorChoose</a>.</td>
</tr>
<tr>
<td>ICMF_CHOOSE_PREVIEW</td>
<td>Displays a Preview button for the video options. This button previews the compression by using a frame from the stream. This is the same flag used in <a href="/windows/desktop/api/vfw/nf-vfw-iccompressorchoose">ICCompressorChoose</a>.</td>
</tr>
</table>

### -param nStreams

Number of streams that have their options set by the dialog box.

### -param ppavi

Pointer to an array of stream interface pointers. The <i>nStreams</i> parameter indicates the number of pointers in the array.

### -param plpOptions

Pointer to an array of pointers to <a href="/windows/desktop/api/vfw/ns-vfw-avicompressoptions">AVICOMPRESSOPTIONS</a> structures. These structures hold the compression options set by the dialog box. The <i>nStreams</i> parameter indicates the number of pointers in the array.

## -returns

Returns <b>TRUE</b> if the user pressed OK, <b>FALSE</b> for CANCEL, or an error otherwise.

## -remarks

This function presents a standard Compression Options dialog box using <i>hwnd</i> as the parent window handle. When the user is finished selecting the compression options for each stream, the options are returned in the <a href="/windows/desktop/api/vfw/ns-vfw-avicompressoptions">AVICOMPRESSOPTIONS</a> structure in the array referenced by <i>plpOptions</i>. The calling application must pass the interface pointers for the streams in the array referenced by <i>ppavi</i>.

An application must allocate memory for the <a href="/windows/desktop/api/vfw/ns-vfw-avicompressoptions">AVICOMPRESSOPTIONS</a> structures and the array of pointers to these structures.

The argument <i>ppavi</i> contains the address of a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>