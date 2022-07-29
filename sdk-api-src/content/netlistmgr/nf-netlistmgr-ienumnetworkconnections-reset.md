---
UID: NF:netlistmgr.IEnumNetworkConnections.Reset
title: IEnumNetworkConnections::Reset (netlistmgr.h)
description: The Reset method resets the enumeration sequence to the beginning. (IEnumNetworkConnections.Reset)
helpviewer_keywords: ["IEnumNetworkConnections interface [Network Awareness]","Reset method","IEnumNetworkConnections.Reset","IEnumNetworkConnections::Reset","Reset","Reset method [Network Awareness]","Reset method [Network Awareness]","IEnumNetworkConnections interface","netlistmgr/IEnumNetworkConnections::Reset","nla.ienumnetworkconnections_reset"]
old-location: nla\ienumnetworkconnections_reset.htm
tech.root: nla
ms.assetid: 5596f7bb-97c8-4751-92fc-1b1ce584ca49
ms.date: 12/05/2018
ms.keywords: IEnumNetworkConnections interface [Network Awareness],Reset method, IEnumNetworkConnections.Reset, IEnumNetworkConnections::Reset, Reset, Reset method [Network Awareness], Reset method [Network Awareness],IEnumNetworkConnections interface, netlistmgr/IEnumNetworkConnections::Reset, nla.ienumnetworkconnections_reset
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Netlistmgr.idl
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
 - IEnumNetworkConnections::Reset
 - netlistmgr/IEnumNetworkConnections::Reset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - IEnumNetworkConnections.Reset
---

# IEnumNetworkConnections::Reset


## -description

The <b>Reset</b> method resets the enumeration sequence to the beginning.



## -returns

Returns S_OK if the method succeeds. Otherwise, the method returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-ienumnetworkconnections">IEnumNetworkConnections</a>
