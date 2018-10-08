---
UID: NF:msacm.acmStreamUnprepareHeader
title: acmStreamUnprepareHeader function
author: windows-sdk-content
description: The acmStreamUnprepareHeader function cleans up the preparation performed by the acmStreamPrepareHeader function for an ACM stream.
old-location: multimedia\acmstreamunprepareheader.htm
tech.root: Multimedia
ms.assetid: 6d693a74-13b6-4923-8267-2e2ecebf78e5
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "_win32_acmStreamUnprepareHeader, acmStreamUnprepareHeader, acmStreamUnprepareHeader function [Windows Multimedia], msacm/acmStreamUnprepareHeader, multimedia.acmstreamunprepareheader"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: msacm.h
req.include-header: 
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
req.lib: Msacm32.lib
req.dll: Msacm32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msacm32.dll
 - Ext-MS-Win-mm-msacm-l1-1-0.dll
api_name:
 - acmStreamUnprepareHeader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# acmStreamUnprepareHeader function


## -description



The <b>acmStreamUnprepareHeader</b> function cleans up the preparation performed by the <a href="https://msdn.microsoft.com/ab90ac5f-6f39-4d26-96fc-5258d4e353cd">acmStreamPrepareHeader</a> function for an ACM stream. This function must be called after the ACM is finished with the given buffers. An application must call this function before freeing the source and destination buffers.




## -parameters




### -param has

Handle to the conversion steam.


### -param pash

Pointer to an <a href="https://msdn.microsoft.com/723e96d8-f098-4e08-862a-a9fea8d2fbe3">ACMSTREAMHEADER</a> structure that identifies the source and destination buffers to be unprepared.


### -param fdwUnprepare

Reserved; must be zero.


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
<dt><b>ACMERR_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The stream header specified in <i>pash</i> is currently in use and cannot be unprepared.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ACMERR_UNPREPARED</b></dt>
</dl>
</td>
<td width="60%">
The stream header specified in <i>pash</i> is currently not prepared by the <a href="https://msdn.microsoft.com/ab90ac5f-6f39-4d26-96fc-5258d4e353cd">acmStreamPrepareHeader</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALFLAG</b></dt>
</dl>
</td>
<td width="60%">
At least one flag is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
At least one parameter is invalid.

</td>
</tr>
</table>
 




## -remarks



Unpreparing a stream header that has already been unprepared is an error. An application must specify the source and destination buffer lengths (<b>cbSrcLength</b> and <b>cbDstLength</b>, respectively) that were used during a call to the corresponding <a href="https://msdn.microsoft.com/ab90ac5f-6f39-4d26-96fc-5258d4e353cd">acmStreamPrepareHeader</a>. Failing to reset these member values will cause <b>acmStreamUnprepareHeader</b> to fail with an MMSYSERR_INVALPARAM error.

The ACM can recover from some errors. The ACM will return a nonzero error, yet the stream header will be properly unprepared. To determine whether the stream header was actually unprepared, an application can examine the ACMSTREAMHEADER_STATUSF_PREPARED flag. If <b>acmStreamUnprepareHeader</b> returns success, the header will always be unprepared.




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

