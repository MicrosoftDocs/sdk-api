---
UID: NF:msclus.ISCluster.get_Resources
title: ISCluster::get_Resources
author: windows-sdk-content
description: Returns a ClusResources collection providing access to the resources in a cluster.
old-location: mscs\cluster_resources.htm
old-project: MsCS
ms.assetid: fdfdd1de-fa4a-4bfb-80e1-15b2141d488b
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: Cluster object [Failover Cluster],Resources property, Cluster.Resources, ISCluster.get_Resources, ISCluster::get_Resources, Resources property [Failover Cluster], Resources property [Failover Cluster],Cluster object, _wolf_cluster.resources, get_Resources, mscs.cluster_resources
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsClus.dll
api_name:
-	Cluster.Resources
-	ISCluster.get_Resources
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISCluster::get_Resources


## -description


<p class="CCE_Message">[The <b>Resources</b> property is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Returns a 
    <a href="https://msdn.microsoft.com/56dd53e7-7e2e-481f-b343-da51c7c52553">ClusResources</a> collection providing access 
    to the <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resources</a> in a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.

This property is read-only.


## -parameters


## -remarks



The <a href="https://msdn.microsoft.com/56dd53e7-7e2e-481f-b343-da51c7c52553">ClusResources</a> collection returned 
    by the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">Cluster</a> object's 
    <b>Resources</b> property provides access to all the 
    resources in the cluster. To retrieve information about all of the resources owned by a particular 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a>, use the 
    <a href="https://msdn.microsoft.com/891a2126-774d-43c6-bd27-6a0e9d943383">ClusResGroup.Resources</a> property.




## -see-also




<a href="https://msdn.microsoft.com/891a2126-774d-43c6-bd27-6a0e9d943383">ClusResGroup.Resources</a>



<a href="https://msdn.microsoft.com/56dd53e7-7e2e-481f-b343-da51c7c52553">ClusResources</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">Cluster</a>
 

 

