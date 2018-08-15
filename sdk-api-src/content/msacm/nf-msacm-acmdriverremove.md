---
UID: NF:msacm.acmDriverRemove
title: acmDriverRemove function
author: windows-sdk-content
description: The acmDriverRemove function removes an ACM driver from the list of available ACM drivers. The driver will be removed for the calling application only. If the driver is globally installed, other applications will still be able to use it.
old-location: multimedia\acmdriverremove.htm
old-project: Multimedia
ms.assetid: 7182d452-a935-4ed5-808a-595fca4f0429
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "_win32_acmDriverRemove, acmDriverRemove, acmDriverRemove function [Windows Multimedia], msacm/acmDriverRemove, multimedia.acmdriverremove"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msacm.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SSTP_CONFIG_PARAMS, *PSSTP_CONFIG_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msacm32.dll
 - Ext-MS-Win-mm-msacm-l1-1-0.dll
api_name:
 - acmDriverRemove
product: Windows
targetos: Windows
req.lib: Msacm32.lib
req.dll: Msacm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# acmDriverRemove function


## -description



The <b>acmDriverRemove</b> function removes an ACM driver from the list of available ACM drivers. The driver will be removed for the calling application only. If the driver is globally installed, other applications will still be able to use it.




## -parameters




### -param hadid

Handle to the driver identifier to be removed.


### -param fdwRemove

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
The driver is in use and cannot be removed.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

