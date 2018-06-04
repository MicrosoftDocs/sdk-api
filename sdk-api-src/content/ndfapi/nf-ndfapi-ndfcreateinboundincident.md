---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# NdfCreateInboundIncident function


## -description


The <b>NdfCreateInboundIncident</b> function creates  a session to diagnose inbound connectivity for a specific application or service.


## -parameters




### -param applicationID [in, optional]

Type: <b>LPCWSTR</b>

The fully qualified path to the application receiving the inbound traffic.


### -param serviceID [in, optional]

Type: <b>LPCWSTR</b>

The Windows service receiving the inbound traffic.



##### dll,-28502 (File/Print Sharing)



##### dll,-28752 (Remote Desktop)



##### dll,-32752 (Network Discovery)


### -param userID [in, optional]

Type: <b>SID*</b>

The SID for the application receiving the traffic. If <b>NULL</b>, the caller's SID is automatically used.


### -param localTarget [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff570825">SOCKADDR_STORAGE</a></b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff570825">SOCKADDR_STORAGE</a> structure which limits the diagnosis to traffic to a specific IP address. If <b>NULL</b>, all traffic will be included in the diagnosis.


### -param protocol

Type: <b>IPPROTO</b>

The protocol which should be diagnosed. For example, IPPROTO_TCP would be used to indicate the TCP/IP protocol.


### -param dwFlags

Type: <b>DWORD</b>

Possible values:



##### )



##### )


### -param handle [out]

Type: <b>NDFHANDLE*</b>

Pointer to a handle to the Network Diagnostics Framework incident.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters has not been provided correctly.


</td>
</tr>
</table>
 




## -remarks



Either <i>applicationID</i> or <i>serviceID</i> must be specified, but not both.



