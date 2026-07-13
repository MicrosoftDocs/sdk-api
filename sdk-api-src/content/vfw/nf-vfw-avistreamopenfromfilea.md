---
UID: NF:vfw.AVIStreamOpenFromFileA
title: AVIStreamOpenFromFileA function (vfw.h)
description: The AVIStreamOpenFromFile function opens a single stream from a file. (ANSI)
helpviewer_keywords: ["AVIStreamOpenFromFileA", "vfw/AVIStreamOpenFromFileA"]
old-location: multimedia\avistreamopenfromfile.htm
tech.root: Multimedia
ms.assetid: f9ac2a8a-08b7-42a7-b71b-a1d44c924b20
ms.date: 12/05/2018
ms.keywords: AVIStreamOpenFromFile, AVIStreamOpenFromFile function [Windows Multimedia], AVIStreamOpenFromFileA, AVIStreamOpenFromFileW, _win32_AVIStreamOpenFromFile, multimedia.avistreamopenfromfile, vfw/AVIStreamOpenFromFile, vfw/AVIStreamOpenFromFileA, vfw/AVIStreamOpenFromFileW
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AVIStreamOpenFromFileW (Unicode) and AVIStreamOpenFromFileA (ANSI)
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
 - AVIStreamOpenFromFileA
 - vfw/AVIStreamOpenFromFileA
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
 - AVIStreamOpenFromFile
 - AVIStreamOpenFromFileA
 - AVIStreamOpenFromFileW
---

# AVIStreamOpenFromFileA function


## -description

The <b>AVIStreamOpenFromFile</b> function opens a single stream from a file.

## -parameters

### -param ppavi

Pointer to a buffer that receives the new stream handle.

### -param szFile

Null-terminated string containing the name of the file to open.

### -param fccType

Four-character code indicating the type of stream to be opened. Zero indicates that any stream can be opened. The following definitions apply to the data commonly found in AVI streams:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>streamtypeAUDIO</td>
<td>Indicates an audio stream.</td>
</tr>
<tr>
<td>streamtypeMIDI</td>
<td>Indicates a MIDI stream.</td>
</tr>
<tr>
<td>streamtypeTEXT</td>
<td>Indicates a text stream.</td>
</tr>
<tr>
<td>streamtypeVIDEO</td>
<td>Indicates a video stream.</td>
</tr>
</table>

### -param lParam

Stream of the type specified in <i>fccType</i> to access. This parameter is zero-based; use zero to specify the first occurrence.

### -param mode

Access mode to use when opening the file. This function can open only existing streams, so the OF_CREATE mode flag cannot be used. For more information about the available flags for the <i>mode</i> parameter, see the <b>OpenFile</b> function.

### -param pclsidHandler

Pointer to a class identifier of the handler you want to use. If the value is <b>NULL</b>, the system chooses one from the registry based on the file extension or the file RIFF type.

## -returns

Returns zero if successful or an error otherwise.

## -remarks

This function calls the <a href="/windows/desktop/api/vfw/nf-vfw-avifileopen">AVIFileOpen</a>, <a href="/windows/desktop/api/vfw/nf-vfw-avifilegetstream">AVIFileGetStream</a>, and <a href="/windows/desktop/api/vfw/nf-vfw-avifilerelease">AVIFileRelease</a> functions.





> [!NOTE]
> The vfw.h header defines AVIStreamOpenFromFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>
