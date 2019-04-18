---
UID: NF:mmiscapi.mmioGetInfo
title: mmioGetInfo function (mmiscapi.h)
author: windows-sdk-content
description: The mmioGetInfo function retrieves information about a file opened by using the mmioOpen function. This information allows the application to directly access the I/O buffer, if the file is opened for buffered I/O.
old-location: multimedia\mmiogetinfo.htm
tech.root: Multimedia
ms.assetid: 9ca58586-8cd6-4d74-9cef-f0ae41b24fe3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_mmioGetInfo, mmioGetInfo, mmioGetInfo function [Windows Multimedia], mmsystem/mmioGetInfo, multimedia.mmiogetinfo"
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
 - mmioGetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# mmioGetInfo function


## -description



The <b>mmioGetInfo</b> function retrieves information about a file opened by using the <a href="https://msdn.microsoft.com/7361f0f2-1c3c-49f1-aec1-2927e05ef0f0">mmioOpen</a> function. This information allows the application to directly access the I/O buffer, if the file is opened for buffered I/O.




## -parameters




### -param hmmio

File handle of the file.


### -param pmmioinfo

Pointer to a buffer that receives an <a href="https://msdn.microsoft.com/44a46d1c-9c9c-42ee-8a2b-ac5b1bc19560">MMIOINFO</a> structure that <b>mmioGetInfo</b> fills with information about the file.


### -param fuInfo

Reserved; must be zero.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



To directly access the I/O buffer of a file opened for buffered I/O, use the following members of the <a href="https://msdn.microsoft.com/44a46d1c-9c9c-42ee-8a2b-ac5b1bc19560">MMIOINFO</a> structure filled by <b>mmioGetInfo</b>:

<ul>
<li>The <b>pchNext</b> member points to the next byte in the buffer that can be read or written. When you read or write, increment <b>pchNext</b> by the number of bytes read or written.</li>
<li>The <b>pchEndRead</b> member points to 1 byte past the last valid byte in the buffer that can be read.</li>
<li>The <b>pchEndWrite</b> member points to 1 byte past the last location in the buffer that can be written.</li>
</ul>
After you read or write to the buffer and modify <b>pchNext</b>, do not call any multimedia file I/O functions except <a href="https://msdn.microsoft.com/30c0b014-a0ac-4002-aeef-24816673f1ed">mmioAdvance</a> until you call the <a href="https://msdn.microsoft.com/3b46ebd6-15e0-4b16-b967-0271946390db">mmioSetInfo</a> function. Call <b>mmioSetInfo</b> when you are finished directly accessing the buffer.

When you reach the end of the buffer specified by the <b>pchEndRead</b> or <b>pchEndWrite</b> member, call <a href="https://msdn.microsoft.com/30c0b014-a0ac-4002-aeef-24816673f1ed">mmioAdvance</a> to fill the buffer from the disk or write the buffer to the disk. The <b>mmioAdvance</b> function updates the <b>pchNext</b>, <b>pchEndRead</b>, and <b>pchEndWrite</b> members in the <a href="https://msdn.microsoft.com/44a46d1c-9c9c-42ee-8a2b-ac5b1bc19560">MMIOINFO</a> structure for the file.

Before calling <a href="https://msdn.microsoft.com/30c0b014-a0ac-4002-aeef-24816673f1ed">mmioAdvance</a> or <a href="https://msdn.microsoft.com/3b46ebd6-15e0-4b16-b967-0271946390db">mmioSetInfo</a> to flush a buffer to disk, set the MMIO_DIRTY flag in the <b>dwFlags</b> member of the <a href="https://msdn.microsoft.com/44a46d1c-9c9c-42ee-8a2b-ac5b1bc19560">MMIOINFO</a> structure for the file. Otherwise, the buffer will not be written to disk.

Do not decrement <b>pchNext</b> or modify any members in the <a href="https://msdn.microsoft.com/44a46d1c-9c9c-42ee-8a2b-ac5b1bc19560">MMIOINFO</a> structure other than <b>pchNext</b> and <b>dwFlags</b>. Do not set any flags in <b>dwFlags</b> except MMIO_DIRTY.



