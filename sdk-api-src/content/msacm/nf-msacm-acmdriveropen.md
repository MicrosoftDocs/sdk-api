---
UID: NF:msacm.acmDriverOpen
title: acmDriverOpen function
author: windows-driver-content
description: The acmDriverOpen function opens the specified ACM driver and returns a driver instance handle that can be used to communicate with the driver.
old-location: multimedia\acmdriveropen.htm
old-project: Multimedia
ms.assetid: a2b98e82-be7a-4e14-bc74-4926eb663ef9
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: "_win32_acmDriverOpen, acmDriverOpen, acmDriverOpen function [Windows Multimedia], msacm/acmDriverOpen, multimedia.acmdriveropen"
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
-	acmDriverOpen
product: Windows
targetos: Windows
req.lib: Msacm32.lib
req.dll: Msacm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# acmDriverOpen function


## -description



The <b>acmDriverOpen</b> function opens the specified ACM driver and returns a driver instance handle that can be used to communicate with the driver.




## -parameters




### -param phad

Pointer to a buffer that receives the new driver instance handle that can be used to communicate with the driver.


### -param hadid

Handle to the driver identifier of an installed and enabled ACM driver.


### -param fdwOpen

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
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOTENABLED</b></dt>
</dl>
</td>
<td width="60%">
The driver is not enabled.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

