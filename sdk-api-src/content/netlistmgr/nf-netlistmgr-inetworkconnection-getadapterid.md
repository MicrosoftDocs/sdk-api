---
UID: NF:netlistmgr.INetworkConnection.GetAdapterId
title: INetworkConnection::GetAdapterId (netlistmgr.h)
author: windows-sdk-content
description: The GetAdapterID method returns the ID of the network adapter used by this connection.
old-location: nla\inetworkconnection_getadapterid.htm
tech.root: nla
ms.assetid: 69711dea-e0dd-4c1e-a83f-1f06d4259b35
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAdapterId, GetAdapterId method [Network Awareness], GetAdapterId method [Network Awareness],INetworkConnection interface, INetworkConnection interface [Network Awareness],GetAdapterId method, INetworkConnection.GetAdapterId, INetworkConnection::GetAdapterId, netlistmgr/INetworkConnection::GetAdapterId, nla.inetworkconnection_getadapterid
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
 - INetworkConnection.GetAdapterId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetworkConnection::GetAdapterId


## -description


The <b>GetAdapterID</b> method returns the ID of the network adapter used by this connection. 


## -parameters




### -param pgdAdapterId [out]

Pointer to a GUID that specifies the adapter ID of the TCP/IP  interface used by this network connection. 


## -returns



Returns S_OK if the method succeeds.




## -remarks



It is possible for multiple connections to have the same AdapterID.




## -see-also




<a href="https://msdn.microsoft.com/666761b5-0146-438d-9986-ecce3b45b5ff">INetworkConnection</a>
 

 

