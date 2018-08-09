---
UID: NF:msclus.ISClusResource.RemoveResourceNode
title: ISClusResource::RemoveResourceNode
author: windows-sdk-content
description: Removes a node from the list of possible nodes that can host the resource.
old-location: mscs\clusresource_removeresourcenode.htm
old-project: mscs
ms.assetid: 4ec493da-4524-4015-8aa7-fb4a8c3d78de
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusResource class [Failover Cluster],RemoveResourceNode method, ClusResource.RemoveResourceNode, ISClusResource.RemoveResourceNode, ISClusResource::RemoveResourceNode, RemoveResourceNode, RemoveResourceNode method [Failover Cluster], RemoveResourceNode method [Failover Cluster],ClusResource class, _wolf_clusresource.removeresourcenode, mscs.clusresource_removeresourcenode
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
 - ClusResource.RemoveResourceNode
 - ISClusResource.RemoveResourceNode
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResource::RemoveResourceNode


## -description


<p class="CCE_Message">[The 
    <b>RemoveResourceNode</b> method is available 
    for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Removes 
    a <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> from the list of possible nodes that can host the 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>.


## -parameters




### -param pNode






#### - Node

The <a href="https://msdn.microsoft.com/b164f5a6-13f1-4eff-a2f9-805b60138dd1">ClusNode</a> object to be removed.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/b164f5a6-13f1-4eff-a2f9-805b60138dd1">ClusNode</a>



<a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a>
 

 

