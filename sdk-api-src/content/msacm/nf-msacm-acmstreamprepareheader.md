---
UID: NF:msacm.acmStreamPrepareHeader
title: acmStreamPrepareHeader function
author: windows-sdk-content
description: The acmStreamPrepareHeader function prepares an ACMSTREAMHEADER structure for an ACM stream conversion.
old-location: multimedia\acmstreamprepareheader.htm
tech.root: Multimedia
ms.assetid: ab90ac5f-6f39-4d26-96fc-5258d4e353cd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_win32_acmStreamPrepareHeader, acmStreamPrepareHeader, acmStreamPrepareHeader function [Windows Multimedia], msacm/acmStreamPrepareHeader, multimedia.acmstreamprepareheader"
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
 - acmStreamPrepareHeader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# acmStreamPrepareHeader function


## -description



The <b>acmStreamPrepareHeader</b> function prepares an <a href="https://msdn.microsoft.com/723e96d8-f098-4e08-862a-a9fea8d2fbe3">ACMSTREAMHEADER</a> structure for an ACM stream conversion. This function must be called for every stream header before it can be used in a conversion stream. An application needs to prepare a stream header only once for the life of a given stream. The stream header can be reused as long as the sizes of the source and destination buffers do not exceed the sizes used when the stream header was originally prepared.




## -parameters




### -param has

Handle to the conversion steam.


### -param pash

Pointer to an <a href="https://msdn.microsoft.com/723e96d8-f098-4e08-862a-a9fea8d2fbe3">ACMSTREAMHEADER</a> structure that identifies the source and destination buffers to be prepared.


### -param fdwPrepare

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
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOMEM</b></dt>
</dl>
</td>
<td width="60%">
The system is unable to allocate resources.

</td>
</tr>
</table>
 




## -remarks



Preparing a stream header that has already been prepared has no effect, and the function returns zero. Nevertheless, you should ensure your application does not prepare a stream header multiple times.




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

