---
UID: NF:msclus.ISClusNetwork.get_NetworkID
title: ISClusNetwork::get_NetworkID
author: windows-sdk-content
description: Unique network identifier for a network.
old-location: mscs\clusnetwork_networkid.htm
old-project: mscs
ms.assetid: c9091461-c6cf-4b2f-97ad-3fb639a09f5e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusNetwork object [Failover Cluster],NetworkID property, ClusNetwork.NetworkID, ISClusNetwork.get_NetworkID, ISClusNetwork::get_NetworkID, NetworkID property [Failover Cluster], NetworkID property [Failover Cluster],ClusNetwork object, _wolf_clusnetwork.networkid, get_NetworkID, mscs.clusnetwork_networkid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsClus.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsClus.tlb
tech.root: 
req.typenames: CLUS_GROUP_START_SETTING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsClus.dll
api_name:
 - ClusNetwork.NetworkID
 - ISClusNetwork.get_NetworkID
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusNetwork::get_NetworkID


## -description


<p class="CCE_Message">[The <b>NetworkID</b> 
    property is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Returns the 
    unique network identifier for a 
    <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a>.

This property is read-only.


## -parameters


## -remarks



The<b>NetworkID</b> of a network is stored in the 
    <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> under 
    <b>HKEY_LOCAL_MACHINE</b>\<b>Cluster</b>\<b>Networks</b>\<b></b>.




## -see-also




<a href="https://msdn.microsoft.com/c62818db-0766-4962-a8be-9b64ef348503">CLUSCTL_NETWORK_GET_ID</a>



<a href="https://msdn.microsoft.com/d51e9872-eb86-4b0e-b417-1a2e5ac6ee9c">ClusNetwork</a>
 

 

