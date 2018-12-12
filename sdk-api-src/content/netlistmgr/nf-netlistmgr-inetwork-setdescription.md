---
UID: NF:netlistmgr.INetwork.SetDescription
title: INetwork::SetDescription
author: windows-sdk-content
description: The SetDescription method sets or replaces the description for a network.
old-location: nla\inetwork_setdescription.htm
tech.root: nla
ms.assetid: d21fc8ca-d097-4099-8c64-f449d1fd49ef
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: INetwork interface [Network Awareness],SetDescription method, INetwork.SetDescription, INetwork::SetDescription, SetDescription, SetDescription method [Network Awareness], SetDescription method [Network Awareness],INetwork interface, netlistmgr/INetwork::SetDescription, nla.inetwork_setdescription
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
 - INetwork.SetDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetwork::SetDescription


## -description


The <b>SetDescription</b> method sets or replaces the description for a network.


## -parameters




### -param szDescription [in]

Zero-terminated string that contains the description of the network.


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
<i>szDescription</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILENAME_EXCED_RANGE)</b></dt>
</dl>
</td>
<td width="60%">
The given name is too long. 

</td>
</tr>
</table>
 




## -remarks



The maximum length for a network description is 1024 characters.




## -see-also




<a href="https://msdn.microsoft.com/6d483058-f7c4-4a6c-a1a8-816c2fab9994">INetwork</a>
 

 

