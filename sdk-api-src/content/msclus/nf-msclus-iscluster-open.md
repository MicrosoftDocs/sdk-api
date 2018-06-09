---
UID: NF:msclus.ISCluster.Open
title: ISCluster::Open
author: windows-sdk-content
description: Opens a connection to a cluster.
old-location: mscs\cluster_open.htm
old-project: MsCS
ms.assetid: 1f5d9f49-1169-45f2-9f3d-11ce9d8db5ef
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: Cluster object [Failover Cluster],Open method, Cluster.Open, ISCluster.Open, ISCluster::Open, Open, Open method [Failover Cluster], Open method [Failover Cluster],Cluster object, _wolf_cluster.open, mscs.cluster_open
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
 - Cluster.Open
 - ISCluster.Open
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISCluster::Open


## -description


<p class="CCE_Message">[The <b>Open</b> method is available for 
    use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent 
    versions.]

Opens a connection to a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.


## -parameters




### -param bstrClusterName






#### - strClusterName

String specifying the name of the cluster to open. If set to a zero-length string (""), 
      the method connects to the local machine's cluster.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">Cluster</a>
 

 

