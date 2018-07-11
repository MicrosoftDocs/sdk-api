---
UID: NF:msclus.ISClusResource.AddResourceNode
title: ISClusResource::AddResourceNode
author: windows-sdk-content
description: Adds a new node to the list of possible nodes that can host the resource.
old-location: mscs\clusresource_addresourcenode.htm
old-project: mscs
ms.assetid: 98727cb1-238f-4bd8-b83a-e3838f824a16
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: AddResourceNode, AddResourceNode method [Failover Cluster], AddResourceNode method [Failover Cluster],ClusResource class, ClusResource class [Failover Cluster],AddResourceNode method, ClusResource.AddResourceNode, ISClusResource.AddResourceNode, ISClusResource::AddResourceNode, _wolf_clusresource.addresourcenode, mscs.clusresource_addresourcenode
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
 - ClusResource.AddResourceNode
 - ISClusResource.AddResourceNode
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResource::AddResourceNode


## -description


<p class="CCE_Message">[The 
    <b>AddResourceNode</b> method is available for use 
    in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent 
    versions.]

Adds 
    a new <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> to the list of possible nodes that can host the 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>.


## -parameters




### -param pNode






#### - objNode

The <a href="https://msdn.microsoft.com/b164f5a6-13f1-4eff-a2f9-805b60138dd1">ClusNode</a> object to add to the list.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/b164f5a6-13f1-4eff-a2f9-805b60138dd1">ClusNode</a>



<a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a>
 

 

