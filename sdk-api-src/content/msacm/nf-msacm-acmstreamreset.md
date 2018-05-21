---
UID: NF:msacm.acmStreamReset
title: acmStreamReset function
author: windows-driver-content
description: The acmStreamReset function stops conversions for a given ACM stream. All pending buffers are marked as done and returned to the application.
old-location: multimedia\acmstreamreset.htm
old-project: Multimedia
ms.assetid: 641c882e-b9c8-4945-bf8a-f3e70c5d5c64
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: "_win32_acmStreamReset, acmStreamReset, acmStreamReset function [Windows Multimedia], msacm/acmStreamReset, multimedia.acmstreamreset"
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
req.typenames: SSTP_CONFIG_PARAMS, *PSSTP_CONFIG_PARAMS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msacm32.dll
-	Ext-MS-Win-mm-msacm-l1-1-0.dll
api_name:
-	acmStreamReset
product: Windows
targetos: Windows
req.lib: Msacm32.lib
req.dll: Msacm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# acmStreamReset function


## -description



The <b>acmStreamReset</b> function stops conversions for a given ACM stream. All pending buffers are marked as done and returned to the application.




## -parameters




### -param has

Handle to the conversion stream.


### -param fdwReset

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
</table>
 




## -remarks



Resetting an ACM conversion stream is necessary only for asynchronous conversion streams. Resetting a synchronous conversion stream will succeed, but no action will be taken.




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

