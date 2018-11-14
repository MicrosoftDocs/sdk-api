---
UID: NF:ndfapi.NdfCreateWinSockIncident
title: NdfCreateWinSockIncident function
author: windows-sdk-content
description: Provides access to the Winsock Helper Class provided by Microsoft.
old-location: ndf\ndfcreatewinsockincident.htm
tech.root: NDF
ms.assetid: c4cb2713-b656-47a8-9de7-9d33e864a811
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: NdfCreateWinSockIncident, NdfCreateWinSockIncident function [NDF], ndf.ndfcreatewinsockincident, ndfapi/NdfCreateWinSockIncident
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ndfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ndfapi.lib
req.dll: Ndfapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ndfapi.dll
api_name:
 - NdfCreateWinSockIncident
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- NdfCreateWinSockIncident
: 
---

# NdfCreateWinSockIncident function


## -description


The <b>NdfCreateWinSockIncident</b> function provides access to the Winsock Helper Class provided by Microsoft.


## -parameters




### -param sock

Type: <b>SOCKET</b>

A descriptor identifying a connected socket.


### -param host [in, optional]

Type: <b>LPCWSTR</b>

A pointer to the local host.


### -param port

Type: <b>USHORT</b>

The port providing Winsock access.


### -param appId [in, optional]

Type: <b>LPCWSTR</b>

Unique identifier associated with the application.


### -param userId [in, optional]

Type: <b>SID*</b>

Unique identifier associated with the user.


### -param handle [out]

Type: <b>NDFHANDLE*</b>

Handle to the Network Diagnostics Framework incident.


## -returns



Type: <b>HRESULT</b>

Possible return values include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to complete this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NDF_E_BAD_PARAM</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5e5caf41-ca24-42e0-ac22-3b569400c383">NdfCloseIncident</a>



<a href="https://msdn.microsoft.com/8570a0e2-f02f-4812-a5c8-13b6e5feee6f">NdfCreateIncident</a>



<a href="https://msdn.microsoft.com/b65f30c3-53d5-4282-8d38-5723772f15fc">NdfExecuteDiagnosis</a>
 

 

