---
UID: NF:ntmsapi.CancelNtmsOperatorRequest
title: CancelNtmsOperatorRequest function
author: windows-sdk-content
description: The CancelNtmsOperatorRequest function cancels the specified RSM operator request.
old-location: fs\cancelntmsoperatorrequest.htm
tech.root: Rsm
ms.assetid: d0ba65fe-0355-4bd6-b9ad-98e8f7992827
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CancelNtmsOperatorRequest, CancelNtmsOperatorRequest function [Files], _zaw_cancelntmsoperatorrequest, base.cancelntmsoperatorrequest, fs.cancelntmsoperatorrequest, ntmsapi/CancelNtmsOperatorRequest
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - CancelNtmsOperatorRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CancelNtmsOperatorRequest
: 
---

# CancelNtmsOperatorRequest function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>CancelNtmsOperatorRequest</b> function cancels the specified RSM operator request.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpRequestId [in]

Unique identifier of the operator request to be canceled. 




To retrieve the list of existing operator requests, use the 
<a href="https://msdn.microsoft.com/bbbb2888-36f5-4667-90f0-088382ad32f5">EnumerateNtmsObject</a> function. You can also use the identifier returned by the 
<a href="https://msdn.microsoft.com/d2c146d0-f1f9-4810-a489-91b5c4ca3431">SubmitNtmsOperatorRequest</a> function.


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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user that tried to execute this function does not have administrator privileges. Only an administrator of the RSM server can cancel operator requests.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The session handle is missing or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The request identifier is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The request has already been completed or canceled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The operator request object ID was not found. This error can occur if the request ID is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The operator request has been canceled.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb540727(v=VS.85).aspx">Operator Request Functions</a>



<a href="https://msdn.microsoft.com/37f9c9c4-7fb2-4559-94a4-e508b277e69e">SatisfyNtmsOperatorRequest</a>



<a href="https://msdn.microsoft.com/d2c146d0-f1f9-4810-a489-91b5c4ca3431">SubmitNtmsOperatorRequest</a>
 

 

