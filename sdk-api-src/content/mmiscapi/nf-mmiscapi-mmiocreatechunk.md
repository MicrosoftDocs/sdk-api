---
UID: NF:mmiscapi.mmioCreateChunk
title: mmioCreateChunk function (mmiscapi.h)
description: The mmioCreateChunk function creates a chunk in a RIFF file that was opened by using the mmioOpen function.
helpviewer_keywords: ["_win32_mmioCreateChunk","mmioCreateChunk","mmioCreateChunk function [Windows Multimedia]","mmsystem/mmioCreateChunk","multimedia.mmiocreatechunk"]
old-location: multimedia\mmiocreatechunk.htm
tech.root: Multimedia
ms.assetid: 45b03f8c-1b79-4004-b5e1-e739138375c2
ms.date: 12/05/2018
ms.keywords: _win32_mmioCreateChunk, mmioCreateChunk, mmioCreateChunk function [Windows Multimedia], mmsystem/mmioCreateChunk, multimedia.mmiocreatechunk
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
 - mmioCreateChunk
 - mmiscapi/mmioCreateChunk
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
 - mmioCreateChunk
---

# mmioCreateChunk function


## -description

The <b>mmioCreateChunk</b> function creates a chunk in a RIFF file that was opened by using the <a href="/previous-versions/dd757331(v=vs.85)">mmioOpen</a> function. The new chunk is created at the current file position. After the new chunk is created, the current file position is the beginning of the data portion of the new chunk.

## -parameters

### -param hmmio

File handle of an open RIFF file.

### -param pmmcki

Pointer to a buffer that receives a <a href="/previous-versions/dd757312(v=vs.85)">MMCKINFO</a> structure containing information about the chunk to be created.

### -param fuCreate

Flags identifying what type of chunk to create. The following values are defined.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>MMIO_CREATELIST</td>
<td>"LIST" chunk.</td>
</tr>
<tr>
<td>MMIO_CREATERIFF</td>
<td>"RIFF" chunk.</td>
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
<dt><b>MMIOERR_CANNOTSEEK</b></dt>
</dl>
</td>
<td width="60%">
Unable to determine offset of the data portion of the chunk.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMIOERR_CANNOTWRITE</b></dt>
</dl>
</td>
<td width="60%">
Unable to write the chunk header.

</td>
</tr>
</table>

## -remarks

This function cannot insert a chunk into the middle of a file. If an application attempts to create a chunk somewhere other than at the end of a file, <b>mmioCreateChunk</b> overwrites existing information in the file.

The <a href="/previous-versions/dd757312(v=vs.85)">MMCKINFO</a> structure pointed to by the <i>lpck</i> parameter should be set up as follows:

<ul>
<li>The <b>ckid</b> member specifies the chunk identifier. If <i>wFlags</i> includes MMIO_CREATERIFF or MMIO_CREATELIST, this member will be filled by <b>mmioCreateChunk</b>.</li>
<li>The <b>cksize</b> member specifies the size of the data portion of the chunk, including the form type or list type (if any). If this value is not correct when the <a href="/previous-versions/dd757315(v=vs.85)">mmioAscend</a> function is called to mark the end of the chunk, <b>mmioAscend</b> corrects the chunk size.</li>
<li>The <b>fccType</b> member specifies the form type or list type if the chunk is a "RIFF" or "LIST" chunk. If the chunk is not a "RIFF" or "LIST" chunk, this member does not need to be filled in.</li>
<li>The <b>dwDataOffset</b> member does not need to be filled in. The <b>mmioCreateChunk</b> function fills this member with the file offset of the data portion of the chunk.</li>
<li>The <b>dwFlags</b> member does not need to be filled in. The <b>mmioCreateChunk</b> function sets the MMIO_DIRTY flag in <b>dwFlags</b>.</li>
</ul>