---
UID: NF:netlistmgr.IEnumNetworks.Skip
title: IEnumNetworks::Skip
author: windows-sdk-content
description: The Skip method skips over the next specified number of elements in the enumeration sequence.
old-location: nla\ienumnetworks_skip.htm
old-project: NLA
ms.assetid: 9f39e65e-6ff4-4fc5-a7fe-5f83a0b3f5e7
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IEnumNetworks interface [Network Awareness],Skip method, IEnumNetworks.Skip, IEnumNetworks::Skip, Skip, Skip method [Network Awareness], Skip method [Network Awareness],IEnumNetworks interface, netlistmgr/IEnumNetworks::Skip, nla.ienumnetworks_skip
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: NLM_NETWORK_PROPERTY_CHANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Netlistmgr.h
api_name:
-	IEnumNetworks.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumNetworks::Skip


## -description


The <b>Skip</b> method skips over the next specified number of elements in the enumeration sequence.


## -parameters




### -param celt [in]

Number of elements to skip in the enumeration.


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




<a href="https://msdn.microsoft.com/ce2b65e5-89fe-48c9-aa00-373406891d02">IEnumNetworks</a>
 

 

