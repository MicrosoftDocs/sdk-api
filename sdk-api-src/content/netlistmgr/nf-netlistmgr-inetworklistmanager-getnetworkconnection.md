---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# INetworkListManager::GetNetworkConnection


## -description


The <b>GetNetworkConnection</b> method retrieves a network based on a supplied Network Connection ID.


## -parameters




### -param gdNetworkConnectionId [in]

A <b>GUID</b> that specifies the Network Connection ID.


### -param ppNetworkConnection [out, retval]

Pointer to a pointer to the <a href="https://msdn.microsoft.com/666761b5-0146-438d-9986-ecce3b45b5ff">INetworkConnection</a> object associated with the supplied <i>gdNetworkConnectionId</i>.


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
The network associated with the specified network connection ID was not found.

</td>
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
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The specified GUID is invalid.

</td>
</tr>
</table>
 




## -remarks



This method can return <b>S_FALSE</b> if a network connection associated with the specified ID has been removed. 
For example, it is possible for  a client to receive a <a href="https://msdn.microsoft.com/0b245a6e-918c-41de-b33e-87723491e900">INetworkConnectionEvents::NetworkConnectionConnectivityChanged</a> event along with a network connection ID, but find that the network connection has been disconnected or even replaced by the time  <b>INetworkListManager::GetNetworkConnection</b> is called with the provided ID.




## -see-also




<a href="https://msdn.microsoft.com/666761b5-0146-438d-9986-ecce3b45b5ff">INetworkConnection</a>



<a href="https://msdn.microsoft.com/a9f76b6a-ea15-47b7-a4ef-14ea60b7810d">INetworkListManager</a>
 

 

