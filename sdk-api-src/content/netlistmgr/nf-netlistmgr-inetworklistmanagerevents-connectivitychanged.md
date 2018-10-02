---
UID: NF:netlistmgr.INetworkListManagerEvents.ConnectivityChanged
title: INetworkListManagerEvents::ConnectivityChanged
author: windows-sdk-content
description: The NetworkConnectivityChanged method is called when network connectivity related changes occur.
old-location: nla\inetworklistmanagerevents_connectivitychanged.htm
tech.root: NLA
ms.assetid: 12e15b56-61cd-4fc8-bc0c-9942d40bb2da
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ConnectivityChanged, ConnectivityChanged method [Network Awareness], ConnectivityChanged method [Network Awareness],INetworkListManagerEvents interface, INetworkListManagerEvents interface [Network Awareness],ConnectivityChanged method, INetworkListManagerEvents.ConnectivityChanged, INetworkListManagerEvents::ConnectivityChanged, netlistmgr/INetworkListManagerEvents::ConnectivityChanged, nla.inetworklistmanagerevents_connectivitychanged
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
 - INetworkListManagerEvents.ConnectivityChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetworkListManagerEvents::ConnectivityChanged


## -description


The <b>NetworkConnectivityChanged</b> method is called when network connectivity related changes occur.


## -parameters




### -param newConnectivity

TBD




#### - NewConnectivity [in]

An <a href="https://msdn.microsoft.com/72d1f049-3c8d-4332-9bf1-9f49b47cd315">NLM_CONNECTIVITY</a> enumeration value that contains the new connectivity settings of the machine.


## -returns



Returns S_OK if the method succeeds.




## -see-also




<a href="https://msdn.microsoft.com/cdcb661f-5f17-481a-a4b7-db06d53e1b97">INetworkListManagerEvents</a>



<a href="https://msdn.microsoft.com/72d1f049-3c8d-4332-9bf1-9f49b47cd315">NLM_CONNECTIVITY</a>
 

 

