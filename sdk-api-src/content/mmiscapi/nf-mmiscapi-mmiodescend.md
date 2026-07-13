---
UID: NF:mmiscapi.mmioDescend
title: mmioDescend function (mmiscapi.h)
description: The mmioDescend function descends into a chunk of a RIFF file that was opened by using the mmioOpen function. It can also search for a given chunk.
helpviewer_keywords: ["_win32_mmioDescend","mmioDescend","mmioDescend function [Windows Multimedia]","mmsystem/mmioDescend","multimedia.mmiodescend"]
old-location: multimedia\mmiodescend.htm
tech.root: Multimedia
ms.assetid: 7ec730fc-3286-4b83-88ac-d59bda85a6ae
ms.date: 12/05/2018
ms.keywords: _win32_mmioDescend, mmioDescend, mmioDescend function [Windows Multimedia], mmsystem/mmioDescend, multimedia.mmiodescend
req.header: mmiscapi.h
req.include-header: Mmiscapi.h, Windows.h
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
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - mmioDescend
 - mmiscapi/mmioDescend
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-mm-io-l1-1-0.dll
 - Winmm.dll
 - API-MS-Win-mm-misc-l1-1-0.dll
 - winmmbase.dll
 - API-MS-Win-mm-misc-l1-1-1.dll
api_name:
 - mmioDescend
---

# mmioDescend function


## -description

The <b>mmioDescend</b> function descends into a chunk of a RIFF file that was opened by using the <a href="/previous-versions/dd757331(v=vs.85)">mmioOpen</a> function. It can also search for a given chunk.

## -parameters

### -param hmmio

File handle of an open RIFF file.

### -param pmmcki

Pointer to a buffer that receives an <a href="/previous-versions/dd757312(v=vs.85)">MMCKINFO</a> structure.

### -param pmmckiParent

Pointer to an optional application-defined <a href="/previous-versions/dd757312(v=vs.85)">MMCKINFO</a> structure identifying the parent of the chunk being searched for. If this parameter is not <b>NULL</b>, <b>mmioDescend</b> assumes the <b>MMCKINFO</b> structure it refers to was filled when <b>mmioDescend</b> was called to descend into the parent chunk, and <b>mmioDescend</b> searches for a chunk within the parent chunk. Set this parameter to <b>NULL</b> if no parent chunk is being specified.

### -param fuDescend

Search flags. If no flags are specified, <b>mmioDescend</b> descends into the chunk beginning at the current file position. The following values are defined.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>MMIO_FINDCHUNK</td>
<td>Searches for a chunk with the specified chunk identifier.</td>
</tr>
<tr>
<td>MMIO_FINDLIST</td>
<td>Searches for a chunk with the chunk identifier "LIST" and with the specified form type.</td>
</tr>
<tr>
<td>MMIO_FINDRIFF</td>
<td>Searches for a chunk with the chunk identifier "RIFF" and with the specified form type.</td>
</tr>
</table>

## -returns

Returns MMSYSERR_NOERROR if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMIOERR_CHUNKNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The end of the file (or the end of the parent chunk, if given) was reached before the desired chunk was found.

</td>
</tr>
</table>

## -remarks

A "RIFF" chunk consists of a four-byte chunk identifier (type <b>FOURCC</b>), followed by a four-byte chunk size (type <b>DWORD</b>), followed by the data portion of the chunk, followed by a null pad byte if the size of the data portion is odd. If the chunk identifier is "RIFF" or "LIST", the first four bytes of the data portion of the chunk are a form type or list type (type <b>FOURCC</b>).

If you use <b>mmioDescend</b> to search for a chunk, make sure the file position is at the beginning of a chunk before calling the function. The search begins at the current file position and continues to the end of the file. If a parent chunk is specified, the file position should be somewhere within the parent chunk before calling <b>mmioDescend</b>. In this case, the search begins at the current file position and continues to the end of the parent chunk.

If <b>mmioDescend</b> is unsuccessful in searching for a chunk, the current file position is undefined. If <b>mmioDescend</b> is successful, the current file position is changed. If the chunk is a "RIFF" or "LIST" chunk, the new file position will be just after the form type or list type (12 bytes from the beginning of the chunk). For other chunks, the new file position will be the start of the data portion of the chunk (8 bytes from the beginning of the chunk).

The <b>mmioDescend</b> function fills the <a href="/previous-versions/dd757312(v=vs.85)">MMCKINFO</a> structure pointed to by the <i>lpck</i> parameter with the following information:

<ul>
<li>The <b>ckid</b> member is the chunk. If the MMIO_FINDCHUNK, MMIO_FINDRIFF, or MMIO_FINDLIST flag is specified for <b>wFlags</b>, the <a href="/previous-versions/dd757312(v=vs.85)">MMCKINFO</a> structure is also used to pass parameters to <b>mmioDescend</b>. In this case, the <b>ckid</b> member specifies the four-character code of the chunk identifier, form type, or list type to search for.</li>
<li>The <b>cksize</b> member is the size, in bytes, of the data portion of the chunk. The size includes the form type or list type (if any), but does not include the 8-byte chunk header or the pad byte at the end of the data (if any).</li>
<li>The <b>fccType</b> member is the form type if <b>ckid</b> is "RIFF", or the list type if <b>ckid</b> is "LIST". Otherwise, it is <b>NULL</b>.</li>
<li>The <b>dwDataOffset</b> member is the file offset of the beginning of the data portion of the chunk. If the chunk is a "RIFF" chunk or a "LIST" chunk, this member is the offset of the form type or list type.</li>
<li>The <b>dwFlags</b> member contains other information about the chunk. Currently, this information is not used and is set to zero.</li>
</ul>