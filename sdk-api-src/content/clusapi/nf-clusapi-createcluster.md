---
UID: NF:clusapi.CreateCluster
title: CreateCluster function
author: windows-sdk-content
description: Creates and starts a cluster.
old-location: mscs\createcluster.htm
tech.root: mscs
ms.assetid: 672a1573-63e5-4321-a049-25bdafc1b5e0
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: CreateCluster, CreateCluster function [Failover Cluster], PCLUSAPI_CREATE_CLUSTER, PCLUSAPI_CREATE_CLUSTER function [Failover Cluster], clusapi/CreateCluster, clusapi/PCLUSAPI_CREATE_CLUSTER, mscs.createcluster
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - CreateCluster
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateCluster function


## -description


Creates and starts a cluster. The cluster consists of the set of nodes specified, with the 
    <a href="https://msdn.microsoft.com/7b5b9d3f-98ab-419b-936e-26e9e5fc022d">Network Name</a>, 
    <a href="https://msdn.microsoft.com/3ed966f1-0177-4376-a36d-4a2fda327470">IP Address</a>, and 
    <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum resources</a> if specified. The <b>PCLUSAPI_CREATE_CLUSTER</b> type defines a pointer to this function.


## -parameters




### -param pConfig [in]

Address of a <a href="https://msdn.microsoft.com/5fc90422-47e4-44da-a49f-66d4b7712f53">CREATE_CLUSTER_CONFIG</a> 
      structure containing configuration information about the cluster to be created.


### -param pfnProgressCallback [in, optional]

Address of callback function that matches the 
      <a href="https://msdn.microsoft.com/fb7a6991-576c-4c03-aef0-89811fbc1a0d">PCLUSTER_SETUP_PROGRESS_CALLBACK</a> 
      function pointer that will be called periodically to provide progress on the cluster creation.


### -param pvCallbackArg [in, optional]

Argument for the callback function.


## -returns



Handle to the newly created cluster or <b>NULL</b>. A non <b>NULL</b> 
      value does not indicate complete success (all nodes will have been added, but not all 
      <a href="https://msdn.microsoft.com/3ed966f1-0177-4376-a36d-4a2fda327470">IP Address</a> or 
      <a href="https://msdn.microsoft.com/7b5b9d3f-98ab-419b-936e-26e9e5fc022d">Network Name</a> resources may have been created. The parameters 
      passed to the function pointed to by the <i>pfnProgressCallback</i> parameter should be 
      checked.




## -remarks



The <b>PCLUSAPI_CREATE_CLUSTER</b> type defines a pointer to this function and can be 
    used with the <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> function to call this 
    function.

After the <b>CreateCluster</b> function successfully 
    completes, at least 30 seconds should be allowed before the 
    <a href="https://msdn.microsoft.com/e1d3611e-10d1-4858-923a-01633d2ed78b">AddClusterNode</a> function is called to add additional 
    nodes.

The <b>CreateCluster</b> function successfully completes 
    after cluster quorum has been achieved. One or more cluster nodes could be in a 
    <b>ClusterNodeDown</b> or <b>ClusterNodeJoining</b> state for a few 
    seconds.

Before calling the <b>CreateCluster</b> function, 
    the <a href="_com_coinitializeex">CoInitializeEx</a> function must be called specifying 
    both <b>COINIT_MULTITHREADED</b> and <b>COINIT_DISABLE_OLE1DDE</b> for 
    the <i>dwCoInit</i> parameter, as shown in the following code.

<pre class="syntax" xml:space="preserve"><code>CoInitializeEx( NULL, COINIT_MULTITHREADED | COINIT_DISABLE_OLE1DDE );</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/e1d3611e-10d1-4858-923a-01633d2ed78b">AddClusterNode</a>



<a href="https://msdn.microsoft.com/5fc90422-47e4-44da-a49f-66d4b7712f53">CREATE_CLUSTER_CONFIG</a>



<a href="https://msdn.microsoft.com/1b3a3b23-39db-47b7-b4a8-17fc1ee45df6">Cluster Management Functions</a>



<a href="https://msdn.microsoft.com/55e601de-b427-43cd-b7f8-6cc576077e59">DestroyCluster</a>



<a href="https://msdn.microsoft.com/fb7a6991-576c-4c03-aef0-89811fbc1a0d">PCLUSTER_SETUP_PROGRESS_CALLBACK</a>
 

 

