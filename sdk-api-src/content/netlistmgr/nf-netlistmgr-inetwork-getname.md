---
UID: NF:netlistmgr.INetwork.GetName
title: INetwork::GetName (netlistmgr.h)
author: windows-sdk-content
description: The GetName method returns the name of a network.
old-location: nla\inetwork_getname.htm
tech.root: nla
ms.assetid: e0dd843e-5bba-4504-b0af-26c0c1ee73a9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [Network Awareness], GetName method [Network Awareness],INetwork interface, INetwork interface [Network Awareness],GetName method, INetwork.GetName, INetwork::GetName, netlistmgr/INetwork::GetName, nla.inetwork_getname
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
 - INetwork.GetName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetwork::GetName


## -description


The <b>GetName</b> method returns the name of a network.


## -parameters




### -param pszNetworkName [out]

Pointer to the name of the network.


## -returns



Returns S_OK if the method succeeds. Otherwise, the method returns the following value.

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
 

 

