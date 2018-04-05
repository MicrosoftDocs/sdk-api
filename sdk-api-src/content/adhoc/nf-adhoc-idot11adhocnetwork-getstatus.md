---
UID: NF:adhoc.IDot11AdHocNetwork.GetStatus
title: IDot11AdHocNetwork::GetStatus method
author: windows-driver-content
description: Gets the connection status of the network.
old-location: nwifi\idot11adhocnetwork_getstatus.htm
old-project: NativeWiFi
ms.assetid: fd627a36-92b7-478b-8fd5-c328b8e54924
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetStatus method [NativeWIFI], GetStatus method [NativeWIFI], IDot11AdHocNetwork interface, GetStatus,IDot11AdHocNetwork.GetStatus, IDot11AdHocNetwork, IDot11AdHocNetwork interface [NativeWIFI], GetStatus method, IDot11AdHocNetwork::GetStatus, adhoc/IDot11AdHocNetwork::GetStatus, nwifi.idot11adhocnetwork_getstatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: adhoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Adhoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	adhoc.h
api_name:
-	IDot11AdHocNetwork.GetStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDot11AdHocNetwork::GetStatus method


## -description


Gets the connection status of the network.


## -parameters




### -param eStatus [in, out]

A pointer to a  <a href="https://msdn.microsoft.com/194179b9-9bd2-4c2f-ab22-c6b95eebfb43">DOT11_ADHOC_NETWORK_CONNECTION_STATUS</a> value that specifies the connection state.


## -returns



Possible return values include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method could not allocate the memory required to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer passed as a parameter is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2736bb81-b66f-4c09-8c76-ca16f3eab192">IDot11AdHocNetwork</a>
 

 

