---
UID: NF:netlistmgr.INetwork.GetDescription
title: INetwork::GetDescription
author: windows-sdk-content
description: The GetDescription method returns a description string for the network.
old-location: nla\inetwork_getdescription.htm
tech.root: nla
ms.assetid: 7d7c4f04-f11c-48ff-b579-dc4dd7599a6b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDescription, GetDescription method [Network Awareness], GetDescription method [Network Awareness],INetwork interface, INetwork interface [Network Awareness],GetDescription method, INetwork.GetDescription, INetwork::GetDescription, netlistmgr/INetwork::GetDescription, nla.inetwork_getdescription
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - INetwork.GetDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetwork::GetDescription


## -description


The <b>GetDescription</b> method returns a description string for the network. 


## -parameters




### -param pszDescription [out]

Pointer to a string that specifies the text description of the network. This value must be freed using the SysFreeString API.


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
The pointer passed is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6d483058-f7c4-4a6c-a1a8-816c2fab9994">INetwork</a>
 

 

