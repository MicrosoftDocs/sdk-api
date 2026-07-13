---
UID: NF:netlistmgr.IEnumNetworks.Reset
title: IEnumNetworks::Reset (netlistmgr.h)
description: The Reset method resets the enumeration sequence to the beginning. (IEnumNetworks.Reset)
helpviewer_keywords: ["IEnumNetworks interface [Network Awareness]","Reset method","IEnumNetworks.Reset","IEnumNetworks::Reset","Reset","Reset method [Network Awareness]","Reset method [Network Awareness]","IEnumNetworks interface","netlistmgr/IEnumNetworks::Reset","nla.ienumnetworks_reset"]
old-location: nla\ienumnetworks_reset.htm
tech.root: nla
ms.assetid: f866f7e1-385c-476e-baf6-b028592fcd0b
ms.date: 12/05/2018
ms.keywords: IEnumNetworks interface [Network Awareness],Reset method, IEnumNetworks.Reset, IEnumNetworks::Reset, Reset, Reset method [Network Awareness], Reset method [Network Awareness],IEnumNetworks interface, netlistmgr/IEnumNetworks::Reset, nla.ienumnetworks_reset
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
 - IEnumNetworks::Reset
 - netlistmgr/IEnumNetworks::Reset
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
 - IEnumNetworks.Reset
---

# IEnumNetworks::Reset


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

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-ienumnetworks">IEnumNetworks</a>
