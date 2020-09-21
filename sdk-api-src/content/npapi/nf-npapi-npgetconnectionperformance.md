---
UID: NF:npapi.NPGetConnectionPerformance
title: NPGetConnectionPerformance function (npapi.h)
description: Returns information about the expected performance of a connection used to access a network resource. The request can only be for a network resource that is currently connected.
helpviewer_keywords: ["NPGetConnectionPerformance","NPGetConnectionPerformance function [Security]","_mnp_npgetconnectionperformance","npapi/NPGetConnectionPerformance","security.npgetconnectionperformance"]
old-location: security\npgetconnectionperformance.htm
tech.root: security
ms.assetid: 8ab9fa3b-50f4-492d-a352-8e215b2d62c1
ms.date: 12/05/2018
ms.keywords: NPGetConnectionPerformance, NPGetConnectionPerformance function [Security], _mnp_npgetconnectionperformance, npapi/NPGetConnectionPerformance, security.npgetconnectionperformance
req.header: npapi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NPGetConnectionPerformance
 - npapi/NPGetConnectionPerformance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Npapi.h
api_name:
 - NPGetConnectionPerformance
---

# NPGetConnectionPerformance function


## -description

Returns information about the expected performance of a connection used to access a network resource. The request can only be for a network resource that is currently connected.

## -parameters

### -param lpRemoteName [in]

Pointer to the local name or remote name for a connected resource.

### -param lpNetConnectInfo [out]

Pointer to a 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-netconnectinfostruct">NETCONNECTINFOSTRUCT</a> structure, which is filled in by the network provider if the provider has a connection to the network resource. All other fields of this structure, except the <b>cbStructure</b> field, are filled with zeros before the MPR passes the request on to the network providers. As a result, the provider has to write only to fields for which it has information available. Also, for rate values, a value of 1 means that the performance is better than can be represented in the unit.

The information returned may be an estimate. If the network cannot obtain information about the resource on the network, it can return information about the network adapter and its associated performance and then set the <b>dwFlags</b> field accordingly.

## -returns

If the function succeeds, it should return WN_SUCCESS. Otherwise, it should return an error code, which can be one of the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
<i>lpRemoteName</i> is not a connected network resource.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NO_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The network is not present.

</td>
</tr>
</table>