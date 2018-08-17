---
UID: NC:clusapi.PCLUSAPI_CREATE_CLUSTER_CNOLESS
title: PCLUSAPI_CREATE_CLUSTER_CNOLESS
author: windows-sdk-content
description: Creates a cluster without cluster name and IP Address resources.
old-location: mscs\createclustercnoless.htm
old-project: mscs
ms.assetid: AED4CDC5-BE90-4F34-A8E2-DFD0617BC65B
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateClusterCNOless, CreateClusterCNOless function [Failover Cluster], PCLUSAPI_CREATE_CLUSTER_CNOLESS, PCLUSAPI_CREATE_CLUSTER_CNOLESS function [Failover Cluster], clusapi/CreateClusterCNOless, clusapi/PCLUSAPI_CREATE_CLUSTER_CNOLESS, mscs.createclustercnoless
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: clusapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - CreateClusterCNOless
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# PCLUSAPI_CREATE_CLUSTER_CNOLESS callback function


## -description


Creates a cluster without <a href="https://msdn.microsoft.com/en-us/library/Aa371733(v=VS.85).aspx">cluster name</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa370484(v=VS.85).aspx">IP Address</a>  resources. The allows you to create clusters that are domain joined but not managed by Active Directory, and clusters that are not members of a domain. <b>PCLUSAPI_CREATE_CLUSTER_CNOLESS</b> defines a pointer to this function.


## -parameters




### -param pConfig [in]

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Bb309213(v=VS.85).aspx">CREATE_CLUSTER_CONFIG</a> structure that contains the cluster configuration.


### -param pfnProgressCallback [in, optional]

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Bb394687(v=VS.85).aspx">ClusterSetupProgressCallback</a> callback function that receives the status of updates to the cluster.


### -param pvCallbackArg [in, optional]

Callback function arguments for the <i>pfnProgressCallback</i> parameter.


## -returns



A handle to the new cluster or <b>NULL</b>. A non <b>NULL</b> 
      value does not indicate success (even if all nodes are added to the cluster, the <a href="https://msdn.microsoft.com/en-us/library/Aa370484(v=VS.85).aspx">IP Address</a> or 
      <a href="https://msdn.microsoft.com/en-us/library/Aa371733(v=VS.85).aspx">Network Name</a> resource creation can fail). After a failure, you should check the parameters 
      passed through the   <i>pfnProgressCallback</i> parameter.




## -remarks



To create clusters that are not domain joined, an non-domain account must have permission to manage the cluster remotely.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa369107(v=VS.85).aspx">Failover Cluster Management Functions</a>
 

 

