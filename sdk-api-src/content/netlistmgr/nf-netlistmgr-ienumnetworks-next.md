---
UID: NF:netlistmgr.IEnumNetworks.Next
title: IEnumNetworks::Next
author: windows-sdk-content
description: The Next method gets the next specified number of elements in the enumeration sequence.
old-location: nla\ienumnetworks_next.htm
old-project: NLA
ms.assetid: 5ee2501c-502e-448e-8635-c8bf9d169ebb
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IEnumNetworks interface [Network Awareness],Next method, IEnumNetworks.Next, IEnumNetworks::Next, Next, Next method [Network Awareness], Next method [Network Awareness],IEnumNetworks interface, netlistmgr/IEnumNetworks::Next, nla.ienumnetworks_next
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
-	IEnumNetworks.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumNetworks::Next


## -description


The <b>Next</b> method gets the next specified number of elements in the enumeration sequence.


## -parameters




### -param celt [in]

Number of elements requested in the enumeration.


### -param rgelt [out]

Pointer to  the enumerated list of pointers returned by <a href="https://msdn.microsoft.com/6d483058-f7c4-4a6c-a1a8-816c2fab9994">INetwork</a>.


### -param pceltFetched [out]

Pointer to the number of elements supplied. This parameter is set to  <b>NULL</b> if <i>celt</i> has the value of 1.


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
The number of elements skipped was not equal to <i>celt</i>.

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




<a href="https://msdn.microsoft.com/ce2b65e5-89fe-48c9-aa00-373406891d02">IEnumNetworks</a>
 

 

