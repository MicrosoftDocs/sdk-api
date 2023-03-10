---
UID: NF:ndfapi.NdfCreateGroupingIncident
title: NdfCreateGroupingIncident function (ndfapi.h)
description: Creates a session to diagnose peer-to-peer grouping functionality issues.
helpviewer_keywords: ["NdfCreateGroupingIncident","NdfCreateGroupingIncident function [NDF]","ndf.ndfcreategroupingincident","ndfapi/NdfCreateGroupingIncident"]
old-location: ndf\ndfcreategroupingincident.htm
tech.root: NDF
ms.assetid: 308aa998-5940-4fbd-8bf6-bb14bc907a3f
ms.date: 12/05/2018
ms.keywords: NdfCreateGroupingIncident, NdfCreateGroupingIncident function [NDF], ndf.ndfcreategroupingincident, ndfapi/NdfCreateGroupingIncident
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
 - NdfCreateGroupingIncident
 - ndfapi/NdfCreateGroupingIncident
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
 - NdfCreateGroupingIncident
---

# NdfCreateGroupingIncident function


## -description

The <b>NdfCreateGroupingIncident</b> function creates  a session to diagnose peer-to-peer grouping functionality issues.

## -parameters

### -param CloudName [in, optional]

Type: <b>LPCWSTR</b>

The name of the Peer Name Resolution Protocol (PNRP) cloud where the group is created. If  <b>NULL</b>, the session will  not attempt to diagnose issues related to PNRP.

### -param GroupName [in, optional]

Type: <b>LPCWSTR</b>

The name of the group to be diagnosed. If <b>NULL</b>, the session will  not attempt to diagnose issues related to group availability.

### -param Identity [in, optional]

Type: <b>LPCWSTR</b>

The identity that a peer uses to access the group. If  <b>NULL</b>, the session will  not attempt to diagnose issues related to the group's ability to register in PNRP.

### -param Invitation [in, optional]

Type: <b>LPCWSTR</b>

An XML invitation granted by another peer. An invitation is created when the inviting peer calls <a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreateinvitation">PeerGroupCreateInvitation</a> or <a href="/windows/desktop/api/p2p/nf-p2p-peergroupissuecredentials">PeerGroupIssueCredentials</a>. If this value is present, the invitation will be checked to ensure its format and expiration are valid.

### -param Addresses [in, optional]

Type: <b>SOCKET_ADDRESS_LIST*</b>

Optional list of addresses of the peers to which the application is trying to connect. If this parameter is used, the helper class will diagnose connectivity to these addresses.

### -param appId [in, optional]

Type: <b>LPCWSTR</b>

Application ID for the calling application.

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
<dt><b>NDF_E_BAD_PARAM</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters has not been provided correctly.


</td>
</tr>
</table>

## -remarks

The level of diagnosis performed depends on the parameters supplied.<ul>
<li>If no parameters are specified, NDF will validate the grouping service status, the status of peer-to-peer services (PNRP and Identity Manager), and Windows clock synchronization.</li>
<li>If <i>CloudName</i> is specified, NDF will validate grouping functionality in that cloud.</li>
<li>If <i>GroupName</i> is specified, NDF will validate that the name can be resolved in PNRP (or invoke the PNRP helper class if the name cannot be resolved) and validate the firewall settings for grouping.</li>
<li>If <i>Identity</i> is specified, NDF will validate PNRP's ability to register the <i>GroupName</i> with this Identity. If this fails, the PNRP helper class will be invoked.</li>
<li>If <i>Invitation</i> is specified, the <i>GroupName</i> will be derived from the Invitation (if a <i>GroupName</i> was not also specified) and NDF will validate the invitation's format and status.</li>
<li>If <i>Addresses</i> is specified, NDF will validate whether Windows can connect to up to three of these addresses.</li>
</ul>