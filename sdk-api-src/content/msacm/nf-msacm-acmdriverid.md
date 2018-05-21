---
UID: NF:msacm.acmDriverID
title: acmDriverID function
author: windows-driver-content
description: The acmDriverID function returns the handle of an ACM driver identifier associated with an open ACM driver instance or stream handle.
old-location: multimedia\acmdriverid.htm
old-project: Multimedia
ms.assetid: d88ec472-80b7-4563-a09d-65e0e829c14e
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: "_win32_acmDriverID, acmDriverID, acmDriverID function [Windows Multimedia], msacm/acmDriverID, multimedia.acmdriverid"
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
-	acmDriverID
product: Windows
targetos: Windows
req.lib: Msacm32.lib
req.dll: Msacm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# acmDriverID function


## -description



The <b>acmDriverID</b> function returns the handle of an ACM driver identifier associated with an open ACM driver instance or stream handle.




## -parameters




### -param hao

Handle to the open driver instance or stream handle. This is the handle of an ACM object, such as <b>HACMDRIVER</b> or <b>HACMSTREAM</b>.


### -param phadid

Pointer to a buffer that receives a handle identifying the installed driver that is associated with <i>hao</i>.


### -param fdwDriverID

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

