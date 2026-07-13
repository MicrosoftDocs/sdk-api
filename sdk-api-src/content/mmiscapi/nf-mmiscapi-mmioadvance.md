---
UID: NF:mmiscapi.mmioAdvance
title: mmioAdvance function (mmiscapi.h)
description: The mmioAdvance function advances the I/O buffer of a file set up for direct I/O buffer access with the mmioGetInfo function.
helpviewer_keywords: ["_win32_mmioAdvance","mmioAdvance","mmioAdvance function [Windows Multimedia]","mmsystem/mmioAdvance","multimedia.mmioadvance"]
old-location: multimedia\mmioadvance.htm
tech.root: Multimedia
ms.assetid: 30c0b014-a0ac-4002-aeef-24816673f1ed
ms.date: 12/05/2018
ms.keywords: _win32_mmioAdvance, mmioAdvance, mmioAdvance function [Windows Multimedia], mmsystem/mmioAdvance, multimedia.mmioadvance
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
 - mmioAdvance
 - mmiscapi/mmioAdvance
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
 - mmioAdvance
---

# mmioAdvance function


## -description

The <b>mmioAdvance</b> function advances the I/O buffer of a file set up for direct I/O buffer access with the <a href="/previous-versions/dd757321(v=vs.85)">mmioGetInfo</a> function.

## -parameters

### -param hmmio

File handle of a file opened by using the <a href="/previous-versions/dd757331(v=vs.85)">mmioOpen</a> function.

### -param pmmioinfo

Pointer to the <a href="/previous-versions/dd757322(v=vs.85)">MMIOINFO</a> structure obtained by using the <a href="/previous-versions/dd757321(v=vs.85)">mmioGetInfo</a> function. This structure is used to set the current file information, and then it is updated after the buffer is advanced. This parameter is optional.

### -param fuAdvance

Flags for the operation. It can be one of the following.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>MMIO_READ</td>
<td>Buffer is filled from the file.</td>
</tr>
<tr>
<td>MMIO_WRITE</td>
<td>Buffer is written to the file.</td>
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
<dt><b>MMIOERR_CANNOTEXPAND</b></dt>
</dl>
</td>
<td width="60%">
The specified memory file cannot be expanded, probably because the <b>adwInfo</b> member of the <a href="/previous-versions/dd757322(v=vs.85)">MMIOINFO</a> structure was set to zero in the initial call to the <a href="/previous-versions/dd757331(v=vs.85)">mmioOpen</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMIOERR_CANNOTREAD</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while refilling the buffer.

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
<tr>
<td width="40%">
<dl>
<dt><b>MMIOERR_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory to expand a memory file for further writing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMIOERR_UNBUFFERED</b></dt>
</dl>
</td>
<td width="60%">
The specified file is not opened for buffered I/O.

</td>
</tr>
</table>

## -remarks

If the file is opened for reading, the I/O buffer is filled from the disk. If the file is opened for writing and the MMIO_DIRTY flag is set in the <b>dwFlags</b> member of the <a href="/previous-versions/dd757322(v=vs.85)">MMIOINFO</a> structure, the buffer is written to disk. The <b>pchNext,</b><b>pchEndRead</b>, and <b>pchEndWrite</b> members of the <b>MMIOINFO</b> structure are updated to reflect the new state of the I/O buffer.

If the specified file is opened for writing or for both reading and writing, the I/O buffer is flushed to disk before the next buffer is read. If the I/O buffer cannot be written to disk because the disk is full, <b>mmioAdvance</b> returns MMIOERR_CANNOTWRITE.

If the specified file is open only for writing, the MMIO_WRITE flag must be specified.

If you have written to the I/O buffer, you must set the MMIO_DIRTY flag in the <b>dwFlags</b> member of the <b>MMIOINFO</b> structure before calling <b>mmioAdvance</b>. Otherwise, the buffer will not be written to disk.

If the end of file is reached, <b>mmioAdvance</b> still returns successfully even though no more data can be read. To check for the end of the file, check if the <b>pchNext</b> and <b>pchEndRead</b> members of the <b>MMIOINFO</b> structure are equal after calling <b>mmioAdvance</b>.