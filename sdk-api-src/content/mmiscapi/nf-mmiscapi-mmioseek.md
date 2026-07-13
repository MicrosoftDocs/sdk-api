---
UID: NF:mmiscapi.mmioSeek
title: mmioSeek function (mmiscapi.h)
description: The mmioSeek function changes the current file position in a file opened by using the mmioOpen function.
helpviewer_keywords: ["SEEK_CUR","SEEK_END","SEEK_SET","_win32_mmioSeek","mmioSeek","mmioSeek function [Windows Multimedia]","mmsystem/mmioSeek","multimedia.mmioseek"]
old-location: multimedia\mmioseek.htm
tech.root: Multimedia
ms.assetid: 11ef0ba9-0b8d-4c1c-981b-3cef5b6ee0e9
ms.date: 12/05/2018
ms.keywords: SEEK_CUR, SEEK_END, SEEK_SET, _win32_mmioSeek, mmioSeek, mmioSeek function [Windows Multimedia], mmsystem/mmioSeek, multimedia.mmioseek
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
 - mmioSeek
 - mmiscapi/mmioSeek
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
 - mmioSeek
---

# mmioSeek function


## -description

The <b>mmioSeek</b> function changes the current file position in a file opened by using the <a href="/previous-versions/dd757331(v=vs.85)">mmioOpen</a> function.

## -parameters

### -param hmmio

File handle of the file to seek in.

### -param lOffset

Offset to change the file position.

### -param iOrigin

Flags indicating how the offset specified by <i>lOffset</i> is interpreted. The following values are defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="SEEK_CUR"></a><a id="seek_cur"></a><dl>
<dt><b>SEEK_CUR</b></dt>
</dl>
</td>
<td width="60%">
Seeks to <i>lOffset</i> bytes from the current file position.

</td>
</tr>
<tr>
<td width="40%"><a id="SEEK_END"></a><a id="seek_end"></a><dl>
<dt><b>SEEK_END</b></dt>
</dl>
</td>
<td width="60%">
Seeks to <i>lOffset</i> bytes from the end of the file.

</td>
</tr>
<tr>
<td width="40%"><a id="SEEK_SET"></a><a id="seek_set"></a><dl>
<dt><b>SEEK_SET</b></dt>
</dl>
</td>
<td width="60%">
Seeks to <i>lOffset</i> bytes from the beginning of the file.

</td>
</tr>
</table>

## -returns

Returns the new file position, in bytes, relative to the beginning of the file. If there is an error, the return value is –1.

## -remarks

Seeking to an invalid location in the file, such as past the end of the file, might not cause <b>mmioSeek</b> to return an error, but it might cause subsequent I/O operations on the file to fail.

To locate the end of a file, call <b>mmioSeek</b> with <i>lOffset</i> set to zero and <i>iOrigin</i> set to SEEK_END.