---
UID: NF:netlistmgr.INetwork.GetTimeCreatedAndConnected
title: INetwork::GetTimeCreatedAndConnected method
author: windows-driver-content
description: The GetTimeCreatedAndConnected method returns the local date and time when the network was created and connected.
old-location: nla\inetwork_gettimecreatedandconnected.htm
old-project: NLA
ms.assetid: 607ce0be-fe7e-4969-b9d0-db1def054f67
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetTimeCreatedAndConnected method [Network Awareness], GetTimeCreatedAndConnected method [Network Awareness], INetwork interface, GetTimeCreatedAndConnected,INetwork.GetTimeCreatedAndConnected, INetwork, INetwork interface [Network Awareness], GetTimeCreatedAndConnected method, INetwork::GetTimeCreatedAndConnected, netlistmgr/INetwork::GetTimeCreatedAndConnected, nla.inetwork_gettimecreatedandconnected
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
-	INetwork.GetTimeCreatedAndConnected
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# INetwork::GetTimeCreatedAndConnected method


## -description


The <b>GetTimeCreatedAndConnected</b> method returns the local date and time when the network was created and connected.


## -parameters




### -param pdwLowDateTimeCreated [out]

Pointer to a datetime when  the network was created. Specifically, it contains the  low DWORD of <b>FILETIME.dwLowDateTime</b>.


### -param pdwHighDateTimeCreated [out]

Pointer to a datetime when  the network was created. Specifically, it contains the  high DWORD of <b>FILETIME.dwLowDateTime</b>.


### -param pdwLowDateTimeConnected [out]

Pointer to a datetime when the network was last connected to. Specifically, it contains the  low DWORD of <b>FILETIME.dwLowDateTime</b>.


### -param pdwHighDateTimeConnected [out]

Pointer to a datetime when the network was last connected to. Specifically, it contains the  high DWORD of <b>FILETIME.dwLowDateTime</b>.


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
 

 

