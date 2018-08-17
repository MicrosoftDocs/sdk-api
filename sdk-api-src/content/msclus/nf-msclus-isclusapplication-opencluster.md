---
UID: NF:msclus.ISClusApplication.OpenCluster
title: ISClusApplication::OpenCluster
author: windows-sdk-content
description: Opens a connection to a cluster.
old-location: mscs\clusapplication_opencluster.htm
old-project: mscs
ms.assetid: 2501e921-5b0a-429f-aa7f-56191ab9795b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ISClusApplication object [Failover Cluster],OpenCluster method, ISClusApplication.OpenCluster, ISClusApplication::OpenCluster, OpenCluster, OpenCluster method [Failover Cluster], OpenCluster method [Failover Cluster],ISClusApplication object, _wolf_clusapplication.opencluster, mscs.clusapplication_opencluster
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msclus.h
req.include-header: 
req.redist: 
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
 - ISClusApplication.OpenCluster
 - ISClusApplication.OpenCluster
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusApplication::OpenCluster


## -description


<p class="CCE_Message">[The <b>OpenCluster</b> 
    method is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Opens a 
    connection to a <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>.


## -parameters




### -param bstrClusterName




### -param pCluster






#### - strClusterName

<b>String</b> containing the name of the cluster to open. If set to a zero-length 
      string (""), the method will open a connection to the local 
      <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node's</a> cluster.


## -returns



A <a href="https://msdn.microsoft.com/4a765dce-c823-4a79-8608-ff41feec8a39">Cluster</a> object that receives the opened 
      connection.




## -see-also




<a href="https://msdn.microsoft.com/2f837658-18f5-44c9-b743-1980a616e71a">ClusApplication</a>



<a href="https://msdn.microsoft.com/4a765dce-c823-4a79-8608-ff41feec8a39">Cluster</a>
 

 

