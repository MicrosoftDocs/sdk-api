---
UID: NF:netlistmgr.IEnumNetworkConnections.Reset
title: IEnumNetworkConnections::Reset method
author: windows-driver-content
description: The Reset method resets the enumeration sequence to the beginning.
old-location: nla\ienumnetworkconnections_reset.htm
old-project: NLA
ms.assetid: 5596f7bb-97c8-4751-92fc-1b1ce584ca49
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IEnumNetworkConnections, IEnumNetworkConnections interface [Network Awareness], Reset method, IEnumNetworkConnections::Reset, Reset method [Network Awareness], Reset method [Network Awareness], IEnumNetworkConnections interface, Reset,IEnumNetworkConnections.Reset, netlistmgr/IEnumNetworkConnections::Reset, nla.ienumnetworkconnections_reset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: NLM_NETWORK_PROPERTY_CHANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Netlistmgr.h
api_name:
-	IEnumNetworkConnections.Reset
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IEnumNetworkConnections::Reset method


## -description


The <b>Reset</b> method resets the enumeration sequence to the beginning.


## -parameters






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




<a href="https://msdn.microsoft.com/f7e69ede-c567-4285-a017-096c94fb3fe4">IEnumNetworkConnections</a>
 

 

