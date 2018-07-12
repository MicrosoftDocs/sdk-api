---
UID: NF:msclus.ISClusNode.get_ResourceGroups
title: ISClusNode::get_ResourceGroups
author: windows-sdk-content
description: Returns a ClusResGroups collection providing access to the groups currently owned by the node.
old-location: mscs\clusnode_resourcegroups.htm
old-project: mscs
ms.assetid: 45eae46b-54d2-4945-aab1-8b471df64881
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: ClusNode object [Failover Cluster],ResourceGroups property, ClusNode.ResourceGroups, ISClusNode.get_ResourceGroups, ISClusNode::get_ResourceGroups, ResourceGroups property [Failover Cluster], ResourceGroups property [Failover Cluster],ClusNode object, _wolf_clusnode.resourcegroups, get_ResourceGroups, mscs.clusnode_resourcegroups
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
 - ClusNode.ResourceGroups
 - ISClusNode.get_ResourceGroups
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusNode::get_ResourceGroups


## -description


<p class="CCE_Message">[The <b>ResourceGroups</b> 
    property is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Returns a <a href="https://msdn.microsoft.com/7411d5f9-15c0-4c03-9128-c6b636979a50">ClusResGroups</a> 
    collection providing access to the <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">groups</a> currently owned by the 
    <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>.

This property is read-only.


## -parameters


## -remarks



To retrieve information about all of the groups in the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>, use the 
    <a href="https://msdn.microsoft.com/449e4432-571c-403c-81c7-da50f455224c">Cluster.ResourceGroups</a> property.




## -see-also




<a href="https://msdn.microsoft.com/b164f5a6-13f1-4eff-a2f9-805b60138dd1">ClusNode</a>



<a href="https://msdn.microsoft.com/7411d5f9-15c0-4c03-9128-c6b636979a50">ClusResGroups</a>



<a href="https://msdn.microsoft.com/449e4432-571c-403c-81c7-da50f455224c">Cluster.ResourceGroups</a>
 

 

