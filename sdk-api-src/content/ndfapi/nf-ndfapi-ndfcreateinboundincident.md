---
UID: NF:ndfapi.NdfCreateInboundIncident
title: NdfCreateInboundIncident function (ndfapi.h)
description: Creates a session to diagnose inbound connectivity for a specific application or service.
helpviewer_keywords: ["@FirewallAPI.dll","-28502","@FirewallAPI.dll","-28752","@FirewallAPI.dll","-32752","NDF_INBOUND_FLAG_EDGETRAVERSAL","NDF_INBOUND_FLAG_HEALTHCHECK","NdfCreateInboundIncident","NdfCreateInboundIncident function [NDF]","ndf.ndfcreateinboundincident","ndfapi/NdfCreateInboundIncident"]
old-location: ndf\ndfcreateinboundincident.htm
tech.root: NDF
ms.assetid: 8cc2c605-96b6-4eca-9e18-f3296187a28f
ms.date: 11/19/2020
ms.keywords: '@FirewallAPI.dll,-28502, @FirewallAPI.dll,-28752, @FirewallAPI.dll,-32752, NDF_INBOUND_FLAG_EDGETRAVERSAL, NDF_INBOUND_FLAG_HEALTHCHECK, NdfCreateInboundIncident, NdfCreateInboundIncident function [NDF], ndf.ndfcreateinboundincident, ndfapi/NdfCreateInboundIncident'
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NdfCreateInboundIncident
 - ndfapi/NdfCreateInboundIncident
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ndfapi.dll
api_name:
 - NdfCreateInboundIncident
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

Type: <b>const <a href="/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)">SOCKADDR_STORAGE</a></b>

A <a href="/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)">SOCKADDR_STORAGE</a> structure which limits the diagnosis to traffic to a specific IP address. If <b>NULL</b>, all traffic will be included in the diagnosis.

### -param protocol

Type: <b>IPPROTO</b>

The protocol which should be diagnosed. For example, IPPROTO_TCP would be used to indicate the TCP/IP protocol.

### -param dwFlags

Type: <b>DWORD</b>

Possible values:

**NDF_INBOUND_FLAG_EDGETRAVERSAL**

Indicates that a configuration should be considered unhealthy if both gateways on the local network are within the private access range, rather than only considering the configuration to be healthy if both gateways are Internet Gateway Devices (IGDs).

**NDF_INBOUND_FLAG_HEALTHCHECK**

Ends the session immediately if no inbound traffic problems are diagnosed, instead of turning on detailed tracing and allowing the user to reproduce their problem for a second diagnosis. 



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