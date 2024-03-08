---
UID: NF:netlistmgr.IEnumNetworkConnections.Next
title: IEnumNetworkConnections::Next (netlistmgr.h)
description: The Next method gets the next specified number of elements in the enumeration sequence. (IEnumNetworkConnections.Next)
helpviewer_keywords: ["IEnumNetworkConnections interface [Network Awareness]","Next method","IEnumNetworkConnections.Next","IEnumNetworkConnections::Next","Next","Next method [Network Awareness]","Next method [Network Awareness]","IEnumNetworkConnections interface","netlistmgr/IEnumNetworkConnections::Next","nla.ienumnetworkconnections_next"]
old-location: nla\ienumnetworkconnections_next.htm
tech.root: nla
ms.assetid: 1c5b35f2-b738-4d23-b90f-87cb559877b5
ms.date: 12/05/2018
ms.keywords: IEnumNetworkConnections interface [Network Awareness],Next method, IEnumNetworkConnections.Next, IEnumNetworkConnections::Next, Next, Next method [Network Awareness], Next method [Network Awareness],IEnumNetworkConnections interface, netlistmgr/IEnumNetworkConnections::Next, nla.ienumnetworkconnections_next
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
 - IEnumNetworkConnections::Next
 - netlistmgr/IEnumNetworkConnections::Next
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
 - IEnumNetworkConnections.Next
---

# IEnumNetworkConnections::Next


## -description

The <b>Next</b> method gets the next specified number of elements in the enumeration sequence.

## -parameters

### -param celt [in]

Number of elements requested.

### -param rgelt [out]

Pointer to a list of pointers returned  by <a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworkconnection">INetworkConnection</a>.

### -param pceltFetched [out]

Pointer to the number of elements supplied. May be <b>NULL</b> if <i>celt</i> is one.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppElements</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-ienumnetworkconnections">IEnumNetworkConnections</a>
