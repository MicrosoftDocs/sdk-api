---
UID: NF:mmiscapi.mmioClose
title: mmioClose function
author: windows-sdk-content
description: The mmioClose function closes a file that was opened by using the mmioOpen function.
old-location: multimedia\mmioclose.htm
tech.root: Multimedia
ms.assetid: 90cc83b5-cd2c-41f1-8bb1-b51bcc894f80
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "_win32_mmioClose, mmioClose, mmioClose function [Windows Multimedia], mmsystem/mmioClose, multimedia.mmioclose"
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
 - mmioClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# mmioClose function


## -description



The <b>mmioClose</b> function closes a file that was opened by using the <a href="https://msdn.microsoft.com/7361f0f2-1c3c-49f1-aec1-2927e05ef0f0">mmioOpen</a> function.




## -parameters




### -param hmmio

File handle of the file to close.


### -param fuClose

TBD




#### - wFlags

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



Returns zero if successful or an error otherwise. The error value can originate from the <a href="https://msdn.microsoft.com/78c2740b-c4fa-4dad-ae4f-0d5b41557669">mmioFlush</a> function or from the I/O procedure. Possible error values include the following.

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
 



