---
UID: NF:mmiscapi.mmioClose
title: mmioClose function (mmiscapi.h)
description: The mmioClose function closes a file that was opened by using the mmioOpen function.
helpviewer_keywords: ["_win32_mmioClose","mmioClose","mmioClose function [Windows Multimedia]","mmsystem/mmioClose","multimedia.mmioclose"]
old-location: multimedia\mmioclose.htm
tech.root: Multimedia
ms.assetid: 90cc83b5-cd2c-41f1-8bb1-b51bcc894f80
ms.date: 12/05/2018
ms.keywords: _win32_mmioClose, mmioClose, mmioClose function [Windows Multimedia], mmsystem/mmioClose, multimedia.mmioclose
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
 - mmioClose
 - mmiscapi/mmioClose
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
 - mmioClose
---

# mmioClose function


## -description

The <b>mmioClose</b> function closes a file that was opened by using the <a href="/previous-versions/dd757331(v=vs.85)">mmioOpen</a> function.

## -parameters

### -param hmmio

File handle of the file to close.

### -param fuClose

Flags for the close operation. The following value is defined.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>MMIO_FHOPEN</td>
<td>If the file was opened by passing a file handle whose type is not <b>HMMIO</b>, using this flag tells the <b>mmioClose</b> function to close the multimedia file handle, but not the standard file handle.</td>
</tr>
</table>

## -returns

Returns zero if successful or an error otherwise. The error value can originate from the <a href="/previous-versions/dd757319(v=vs.85)">mmioFlush</a> function or from the I/O procedure. Possible error values include the following.

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