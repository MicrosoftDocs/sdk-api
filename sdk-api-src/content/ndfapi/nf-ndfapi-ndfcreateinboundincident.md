---
UID: NF:ndfapi.NdfCreateInboundIncident
title: NdfCreateInboundIncident function (ndfapi.h)
author: windows-sdk-content
description: Creates a session to diagnose inbound connectivity for a specific application or service.
old-location: ndf\ndfcreateinboundincident.htm
tech.root: NDF
ms.assetid: 8cc2c605-96b6-4eca-9e18-f3296187a28f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "@FirewallAPI.dll,-28502, @FirewallAPI.dll,-28752, @FirewallAPI.dll,-32752, NDF_INBOUND_FLAG_EDGETRAVERSAL, NDF_INBOUND_FLAG_HEALTHCHECK, NdfCreateInboundIncident, NdfCreateInboundIncident function [NDF], ndf.ndfcreateinboundincident, ndfapi/NdfCreateInboundIncident"
ms.topic: function
req.header: ndfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - NdfCreateInboundIncident
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

Type: <b>const <a href="https://msdn.microsoft.com/dfd84b91-0a94-4fe6-b8d2-18562afb9c24">SOCKADDR_STORAGE</a></b>

A <a href="https://msdn.microsoft.com/dfd84b91-0a94-4fe6-b8d2-18562afb9c24">SOCKADDR_STORAGE</a> structure which limits the diagnosis to traffic to a specific IP address. If <b>NULL</b>, all traffic will be included in the diagnosis.


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



