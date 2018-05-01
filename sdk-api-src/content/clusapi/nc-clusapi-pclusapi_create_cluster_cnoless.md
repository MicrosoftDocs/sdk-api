---
UID: NC:clusapi.PCLUSAPI_CREATE_CLUSTER_CNOLESS
title: PCLUSAPI_CREATE_CLUSTER_CNOLESS
author: windows-driver-content
description: Creates a cluster without cluster name and IP Address resources.
old-location: mscs\createclustercnoless.htm
old-project: MsCS
ms.assetid: AED4CDC5-BE90-4F34-A8E2-DFD0617BC65B
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PCLUSAPI_CREATE_CLUSTER_CNOLESS, PCLUSAPI_CREATE_CLUSTER_CNOLESS callback function [Failover Cluster], clusapi/PCLUSAPI_CREATE_CLUSTER_CNOLESS, mscs.createclustercnoless
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: clusapi.h
req.include-header: 
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
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_CREATE_CLUSTER_CNOLESS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CREATE_CLUSTER_CNOLESS callback


## -description


Creates a cluster without <a href="https://msdn.microsoft.com/7b5b9d3f-98ab-419b-936e-26e9e5fc022d">cluster name</a> and <a href="https://msdn.microsoft.com/3ed966f1-0177-4376-a36d-4a2fda327470">IP Address</a>  resources. The allows you to create clusters that are domain joined but not managed by Active Directory, and clusters that are not members of a domain. <b>PCLUSAPI_CREATE_CLUSTER_CNOLESS</b> defines a pointer to this function.


## -parameters




### -param pConfig [in]

A pointer to the <a href="https://msdn.microsoft.com/5fc90422-47e4-44da-a49f-66d4b7712f53">CREATE_CLUSTER_CONFIG</a> structure that contains the cluster configuration.


### -param pfnProgressCallback [in, optional]

A pointer to the <a href="https://msdn.microsoft.com/fb7a6991-576c-4c03-aef0-89811fbc1a0d">ClusterSetupProgressCallback</a> callback function that receives the status of updates to the cluster.


### -param pvCallbackArg [in, optional]

Callback function arguments for the <i>pfnProgressCallback</i> parameter.


## -returns



A handle to the new cluster or <b>NULL</b>. A non <b>NULL</b> 
      value does not indicate success (even if all nodes are added to the cluster, the <a href="https://msdn.microsoft.com/3ed966f1-0177-4376-a36d-4a2fda327470">IP Address</a> or 
      <a href="https://msdn.microsoft.com/7b5b9d3f-98ab-419b-936e-26e9e5fc022d">Network Name</a> resource creation can fail). After a failure, you should check the parameters 
      passed through the   <i>pfnProgressCallback</i> parameter.




## -remarks



To create clusters that are not domain joined, an non-domain account must have permission to manage the cluster remotely.




## -see-also




<a href="https://msdn.microsoft.com/1b3a3b23-39db-47b7-b4a8-17fc1ee45df6">Failover Cluster Management Functions</a>
 

 

