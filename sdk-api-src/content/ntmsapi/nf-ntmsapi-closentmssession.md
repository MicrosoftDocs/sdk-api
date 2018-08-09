---
UID: NF:ntmsapi.CloseNtmsSession
title: CloseNtmsSession function
author: windows-sdk-content
description: The CloseNtmsSession function closes the specified RSM session.
old-location: fs\closentmssession.htm
old-project: Rsm
ms.assetid: 54bc354a-fdef-4642-8e53-cf20ed374000
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: CloseNtmsSession, CloseNtmsSession function [Files], _zaw_closentmssession, base.closentmssession, fs.closentmssession, ntmsapi/CloseNtmsSession
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - CloseNtmsSession
product: Windows
targetos: Windows
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
req.product: ADAM
---

# CloseNtmsSession function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>CloseNtmsSession</b> function closes the specified RSM session.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


## -returns



This function returns one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CONNECTION_UNAVAIL</b></dt>
</dl>
</td>
<td width="60%">
Connection to the RSM server or domain is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The value specified in the <i>hSession</i> parameter is <b>NULL</b> or is not a valid session handle.

</td>
</tr>
</table>
 




## -remarks



The 
<b>CloseNtmsSession</b> function releases all resources. Use of a closed session handle returns an error code.

If a call to the 
<b>CloseNtmsSession</b> function occurs while an application has an outstanding synchronous request (for example, a mount or dismount request), the request is unwound and canceled.




## -see-also




<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a>



<a href="removable_storage_manager_functions.htm">Session Management Functions</a>
 

 

