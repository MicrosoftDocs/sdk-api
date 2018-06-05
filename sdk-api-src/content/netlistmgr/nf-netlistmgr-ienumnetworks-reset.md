---
UID: NF:netlistmgr.IEnumNetworks.Reset
title: IEnumNetworks::Reset
author: windows-sdk-content
description: The Reset method resets the enumeration sequence to the beginning.
old-location: nla\ienumnetworks_reset.htm
old-project: NLA
ms.assetid: f866f7e1-385c-476e-baf6-b028592fcd0b
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IEnumNetworks interface [Network Awareness],Reset method, IEnumNetworks.Reset, IEnumNetworks::Reset, Reset, Reset method [Network Awareness], Reset method [Network Awareness],IEnumNetworks interface, netlistmgr/IEnumNetworks::Reset, nla.ienumnetworks_reset
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
-	IEnumNetworks.Reset
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumNetworks::Reset


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




<a href="https://msdn.microsoft.com/ce2b65e5-89fe-48c9-aa00-373406891d02">IEnumNetworks</a>
 

 

