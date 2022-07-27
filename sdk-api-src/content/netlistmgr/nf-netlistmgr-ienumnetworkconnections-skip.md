---
UID: NF:netlistmgr.IEnumNetworkConnections.Skip
title: IEnumNetworkConnections::Skip (netlistmgr.h)
description: The Skip method skips over the next specified number of elements in the enumeration sequence. (IEnumNetworkConnections.Skip)
helpviewer_keywords: ["IEnumNetworkConnections interface [Network Awareness]","Skip method","IEnumNetworkConnections.Skip","IEnumNetworkConnections::Skip","Skip","Skip method [Network Awareness]","Skip method [Network Awareness]","IEnumNetworkConnections interface","netlistmgr/IEnumNetworkConnections::Skip","nla.ienumnetworkconnections_skip"]
old-location: nla\ienumnetworkconnections_skip.htm
tech.root: nla
ms.assetid: 0423e39e-6101-47dc-99cc-5920d720e47a
ms.date: 12/05/2018
ms.keywords: IEnumNetworkConnections interface [Network Awareness],Skip method, IEnumNetworkConnections.Skip, IEnumNetworkConnections::Skip, Skip, Skip method [Network Awareness], Skip method [Network Awareness],IEnumNetworkConnections interface, netlistmgr/IEnumNetworkConnections::Skip, nla.ienumnetworkconnections_skip
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
 - IEnumNetworkConnections::Skip
 - netlistmgr/IEnumNetworkConnections::Skip
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
 - IEnumNetworkConnections.Skip
---

# IEnumNetworkConnections::Skip


## -description

The <b>Skip</b> method skips over the next specified number of elements in the enumeration sequence.

## -parameters

### -param celt [in]

Number of elements to skip over in the enumeration.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The number of elements skipped was not <i>celt</i>.

</td>
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
