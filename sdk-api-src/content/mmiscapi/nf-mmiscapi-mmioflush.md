---
UID: NF:mmiscapi.mmioFlush
title: mmioFlush function (mmiscapi.h)
description: The mmioFlush function writes the I/O buffer of a file to disk if the buffer has been written to.
helpviewer_keywords: ["_win32_mmioFlush","mmioFlush","mmioFlush function [Windows Multimedia]","mmsystem/mmioFlush","multimedia.mmioflush"]
old-location: multimedia\mmioflush.htm
tech.root: Multimedia
ms.assetid: 78c2740b-c4fa-4dad-ae4f-0d5b41557669
ms.date: 12/05/2018
ms.keywords: _win32_mmioFlush, mmioFlush, mmioFlush function [Windows Multimedia], mmsystem/mmioFlush, multimedia.mmioflush
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
 - mmioFlush
 - mmiscapi/mmioFlush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
 - API-MS-Win-mm-misc-l1-1-0.dll
 - winmmbase.dll
 - API-MS-Win-mm-misc-l1-1-1.dll
api_name:
 - mmioFlush
---

# mmioFlush function


## -description

The <b>mmioFlush</b> function writes the I/O buffer of a file to disk if the buffer has been written to.

## -parameters

### -param hmmio

File handle of a file opened by using the <a href="/previous-versions/dd757331(v=vs.85)">mmioOpen</a> function.

### -param fuFlush

Flag determining how the flush is carried out. It can be zero or the following.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>MMIO_EMPTYBUF</td>
<td>Empties the buffer after writing it to the disk.</td>
</tr>
</table>

## -returns

Returns zero if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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

Closing a file with the <a href="/previous-versions/dd757316(v=vs.85)">mmioClose</a> function automatically flushes its buffer.

If there is insufficient disk space to write the buffer, <b>mmioFlush</b> fails, even if the preceding calls of the <a href="/previous-versions/dd757341(v=vs.85)">mmioWrite</a> function were successful.