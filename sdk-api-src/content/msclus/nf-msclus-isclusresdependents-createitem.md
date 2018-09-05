---
UID: NF:msclus.ISClusResDependents.CreateItem
title: ISClusResDependents::CreateItem
author: windows-sdk-content
description: Creates a resource in the cluster and adds it to the ClusResDependents collection.
old-location: mscs\clusresdependents_createitem.htm
old-project: mscs
ms.assetid: e696bee0-7ca4-47ec-a29a-b13e445a72de
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CLUSTER_RESOURCE_DEFAULT_MONITOR, CLUSTER_RESOURCE_SEPARATE_MONITOR, ClusResDependents class [Failover Cluster],CreateItem method, ClusResDependents.CreateItem, CreateItem, CreateItem method [Failover Cluster], CreateItem method [Failover Cluster],ClusResDependents class, ISClusResDependents.CreateItem, ISClusResDependents::CreateItem, _wolf_clusresdependents.createitem, mscs.clusresdependents_createitem
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
 - ClusResDependents.CreateItem
 - ISClusResDependents.CreateItem
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResDependents::CreateItem


## -description


<p class="CCE_Message">[The <b>CreateItem</b> 
    method is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Creates a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> in the 
    <a href="c_gly.htm">cluster</a> and adds it to the 
    <a href="https://msdn.microsoft.com/4e1f47fa-e240-4fdb-b736-9b2e64828eb0">ClusResDependents</a> collection.


## -parameters




### -param bstrResourceName




### -param bstrResourceType




### -param dwFlags

Value indicating how to create the resource. <i>Flag</i> can be set to one of the 
      following values enumerated from the 
      <a href="https://msdn.microsoft.com/16f5ab58-2507-431a-98f9-bd00a24485ba">CLUSTER_RESOURCE_CREATE_FLAGS</a> 
      enumeration.



#### CLUSTER_RESOURCE_DEFAULT_MONITOR (0)

The <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a> determines the 
        <a href="https://msdn.microsoft.com/caebb47f-c2c5-463e-a957-d9eefc7fc33d">Resource Monitor</a> to which the new resource will be 
        assigned.



#### CLUSTER_RESOURCE_SEPARATE_MONITOR (1)

Causes the Cluster service to create a separate Resource Monitor dedicated exclusively to the new 
        resource.


### -param ppClusterResource






#### - GroupName

<b>String</b> containing the name of the 
      <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">group</a> to which the new resource will belong.


#### - ResourceName

<b>String</b> containing the name of the resource to create.


#### - ResourceType

<b>String</b> specifying the type of the resource to create.


## -returns



A <a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a> object that receives the new 
      resource.




## -remarks



Resources added to a 
    <a href="https://msdn.microsoft.com/4e1f47fa-e240-4fdb-b736-9b2e64828eb0">ClusResDependents</a> 
    collection become <a href="https://msdn.microsoft.com/2ad913d2-99cb-4885-a1de-822f77dc2030">dependents</a> of the resource from 
    which the collection was obtained.




## -see-also




<a href="https://msdn.microsoft.com/4e1f47fa-e240-4fdb-b736-9b2e64828eb0">ClusResDependents</a>



<a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a>
 

 

