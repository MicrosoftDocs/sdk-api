---
UID: NF:mmiscapi.mmioSetBuffer
title: mmioSetBuffer function
author: windows-sdk-content
description: The mmioSetBuffer function enables or disables buffered I/O, or changes the buffer or buffer size for a file opened by using the mmioOpen function.
old-location: multimedia\mmiosetbuffer.htm
tech.root: Multimedia
ms.assetid: 78bee0a3-1f9e-4268-8070-8267cc6aab5a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_win32_mmioSetBuffer, mmioSetBuffer, mmioSetBuffer function [Windows Multimedia], mmsystem/mmioSetBuffer, multimedia.mmiosetbuffer"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - mmioSetBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# mmioSetBuffer function


## -description



The <b>mmioSetBuffer</b> function enables or disables buffered I/O, or changes the buffer or buffer size for a file opened by using the <a href="https://msdn.microsoft.com/7361f0f2-1c3c-49f1-aec1-2927e05ef0f0">mmioOpen</a> function.




## -parameters




### -param hmmio

File handle of the file.


### -param pchBuffer

Pointer to an application-defined buffer to use for buffered I/O. If this parameter is <b>NULL</b>, <b>mmioSetBuffer</b> allocates an internal buffer for buffered I/O.


### -param cchBuffer

Size, in characters, of the application-defined buffer, or the size of the buffer for <b>mmioSetBuffer</b> to allocate.


### -param fuBuffer

Reserved; must be zero.


## -returns



Returns zero if successful or an error otherwise. If an error occurs, the file handle remains valid. The following values are defined.

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
The contents of the old buffer could not be written to disk, so the operation was aborted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMIOERR_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The new buffer could not be allocated, probably due to a lack of available memory.

</td>
</tr>
</table>
 




## -remarks



To enable buffering using an internal buffer, set <i>pchBuffer</i> to <b>NULL</b> and <i>cchBuffer</i> to the desired buffer size.

To supply your own buffer, set <i>pchBuffer</i> to point to the buffer, and set <i>cchBuffer</i> to the size of the buffer.

To disable buffered I/O, set <i>pchBuffer</i> to <b>NULL</b> and <i>cchBuffer</i> to zero.

If buffered I/O is already enabled using an internal buffer, you can reallocate the buffer to a different size by setting <i>pchBuffer</i> to <b>NULL</b> and <i>cchBuffer</i> to the new buffer size. The contents of the buffer can be changed after resizing.



