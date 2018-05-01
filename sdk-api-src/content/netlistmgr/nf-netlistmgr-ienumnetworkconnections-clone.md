---
UID: NF:netlistmgr.IEnumNetworkConnections.Clone
title: IEnumNetworkConnections::Clone method
author: windows-driver-content
description: The Clone method creates an enumerator that contains the same enumeration state as the enumerator currently in use.
old-location: nla\ienumnetworkconnections_clone.htm
old-project: NLA
ms.assetid: eb59b8ae-b53c-4035-96c4-72cf87edb2eb
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Clone method [Network Awareness], Clone method [Network Awareness], IEnumNetworkConnections interface, Clone,IEnumNetworkConnections.Clone, IEnumNetworkConnections, IEnumNetworkConnections interface [Network Awareness], Clone method, IEnumNetworkConnections::Clone, netlistmgr/IEnumNetworkConnections::Clone, nla.ienumnetworkconnections_clone
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
-	IEnumNetworkConnections.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IEnumNetworkConnections::Clone method


## -description


The <b>Clone</b> method creates an enumerator that contains the same enumeration state as the enumerator currently in use.


## -parameters




### -param ppEnumNetwork [out]

Pointer to new <a href="https://msdn.microsoft.com/f7e69ede-c567-4285-a017-096c94fb3fe4">IEnumNetworkConnections</a> interface instance.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppEnum</i> parameter is not a valid pointer.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Failed for unknown reasons.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f7e69ede-c567-4285-a017-096c94fb3fe4">IEnumNetworkConnections</a>
 

 

