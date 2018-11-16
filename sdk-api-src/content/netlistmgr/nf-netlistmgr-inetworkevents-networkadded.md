---
UID: NF:netlistmgr.INetworkEvents.NetworkAdded
title: INetworkEvents::NetworkAdded
author: windows-sdk-content
description: The NetworkAdded method is called when a new network is added. The GUID of the new network is provided.
old-location: nla\inetworkevents_networkadded.htm
tech.root: NLA
ms.assetid: 2fda364e-ad6a-447a-ba0c-25e5d52ef5c5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: INetworkEvents interface [Network Awareness],NetworkAdded method, INetworkEvents.NetworkAdded, INetworkEvents::NetworkAdded, NetworkAdded, NetworkAdded method [Network Awareness], NetworkAdded method [Network Awareness],INetworkEvents interface, netlistmgr/INetworkEvents::NetworkAdded, nla.inetworkevents_networkadded
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
 - INetworkEvents.NetworkAdded
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- netlistmgr.h
: 
- INetworkEvents.NetworkAdded
: 
---

# INetworkEvents::NetworkAdded


## -description


The <b>NetworkAdded</b> method is called when a new network is added. The GUID of the new network is provided.


## -parameters




### -param networkId [in]

 A <b>GUID</b> that specifies the new network that was added.


## -returns



Returns S_OK if the method succeeds.




## -see-also




<a href="https://msdn.microsoft.com/75cc6efb-dd1b-40b6-84fe-5ba7c244cd72">INetworkEvents</a>
 

 

