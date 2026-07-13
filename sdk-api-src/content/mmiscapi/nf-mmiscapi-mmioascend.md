---
UID: NF:mmiscapi.mmioAscend
title: mmioAscend function (mmiscapi.h)
description: The mmioAscend function ascends out of a chunk in a RIFF file descended into with the mmioDescend function or created with the mmioCreateChunk function.
helpviewer_keywords: ["_win32_mmioAscend","mmioAscend","mmioAscend function [Windows Multimedia]","mmsystem/mmioAscend","multimedia.mmioascend"]
old-location: multimedia\mmioascend.htm
tech.root: Multimedia
ms.assetid: 33da4c65-8ce1-44cf-9d5f-f5626620b420
ms.date: 12/05/2018
ms.keywords: _win32_mmioAscend, mmioAscend, mmioAscend function [Windows Multimedia], mmsystem/mmioAscend, multimedia.mmioascend
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
 - mmioAscend
 - mmiscapi/mmioAscend
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
 - mmioAscend
---

# mmioAscend function


## -description

The <b>mmioAscend</b> function ascends out of a chunk in a RIFF file descended into with the <a href="/previous-versions/dd757318(v=vs.85)">mmioDescend</a> function or created with the <a href="/previous-versions/dd757317(v=vs.85)">mmioCreateChunk</a> function.

## -parameters

### -param hmmio

File handle of an open RIFF file.

### -param pmmcki

Pointer to an application-defined <a href="/previous-versions/dd757312(v=vs.85)">MMCKINFO</a> structure previously filled by the <a href="/previous-versions/dd757318(v=vs.85)">mmioDescend</a> or <a href="/previous-versions/dd757317(v=vs.85)">mmioCreateChunk</a> function.

### -param fuAscend

Reserved; must be zero.

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
There was an error while seeking to the end of the chunk.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMIOERR_CANNOTWRITE</b></dt>
</dl>
</td>
<td width="60%">
The contents of the buffer could not be written to disk.

</td>
</tr>
</table>

## -remarks

If the chunk was descended into by using <a href="/previous-versions/dd757318(v=vs.85)">mmioDescend</a>, <b>mmioAscend</b> seeks to the location following the end of the chunk (past the extra pad byte, if any).

If the chunk was created and descended into by using <b>mmioCreateChunk</b>, or if the MMIO_DIRTY flag is set in the <b>dwFlags</b> member of the <b>MMCKINFO</b> structure referenced by <i>lpck</i>, the current file position is assumed to be the end of the data portion of the chunk. If the chunk size is not the same as the value stored in the <b>cksize</b> member of the <b>MMCKINFO</b> structure when <b>mmioCreateChunk</b> was called, <b>mmioAscend</b> corrects the chunk size in the file before ascending from the chunk. If the chunk size is odd, <b>mmioAscend</b> writes a null pad byte at the end of the chunk. After ascending from the chunk, the current file position is the location following the end of the chunk (past the extra pad byte, if any).