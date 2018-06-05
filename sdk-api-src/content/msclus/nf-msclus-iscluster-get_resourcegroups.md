---
UID: NF:msclus.ISCluster.get_ResourceGroups
title: ISCluster::get_ResourceGroups
author: windows-sdk-content
description: Returns the groups in a cluster.
old-location: mscs\cluster_resourcegroups.htm
old-project: MsCS
ms.assetid: 449e4432-571c-403c-81c7-da50f455224c
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: Cluster object [Failover Cluster],ResourceGroups property, Cluster.ResourceGroups, ISCluster.get_ResourceGroups, ISCluster::get_ResourceGroups, ResourceGroups property [Failover Cluster], ResourceGroups property [Failover Cluster],Cluster object, _wolf_cluster.resourcegroups, get_ResourceGroups, mscs.cluster_resourcegroups
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
-	Cluster.ResourceGroups
-	ISCluster.get_ResourceGroups
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISCluster::get_ResourceGroups


## -description


<p class="CCE_Message">[The <b>ResourceGroups</b> 
    property is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Returns the 
    <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">groups</a> in a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.

This property is read-only.


## -parameters


## -remarks



To access all of the groups for a particular <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>, use the 
    <a href="https://msdn.microsoft.com/45eae46b-54d2-4945-aab1-8b471df64881">ClusNode.ResourceGroups</a> property for that 
    node.




## -see-also




<a href="https://msdn.microsoft.com/45eae46b-54d2-4945-aab1-8b471df64881">ClusNode.ResourceGroups</a>



<a href="https://msdn.microsoft.com/7411d5f9-15c0-4c03-9128-c6b636979a50">ClusResGroups</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">Cluster</a>
 

 

