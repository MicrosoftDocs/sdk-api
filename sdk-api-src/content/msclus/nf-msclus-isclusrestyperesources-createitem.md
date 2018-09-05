---
UID: NF:msclus.ISClusResTypeResources.CreateItem
title: ISClusResTypeResources::CreateItem
author: windows-sdk-content
description: Creates a resource in the cluster and adds it to the ClusResTypeResources collection.
old-location: mscs\clusrestyperesources_createitem.htm
old-project: mscs
ms.assetid: 215482f4-4357-462b-bf67-109cc36e22b7
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CLUSTER_RESOURCE_DEFAULT_MONITOR, CLUSTER_RESOURCE_SEPARATE_MONITOR, ClusResTypeResources class [Failover Cluster],CreateItem method, ClusResTypeResources.CreateItem, CreateItem, CreateItem method [Failover Cluster], CreateItem method [Failover Cluster],ClusResTypeResources class, ISClusResTypeResources.CreateItem, ISClusResTypeResources::CreateItem, _wolf_clusrestyperesources.createitem, mscs.clusrestyperesources_createitem
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
 - ClusResTypeResources.CreateItem
 - ISClusResTypeResources.CreateItem
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResTypeResources::CreateItem


## -description


<p class="CCE_Message">[The 
    <b>CreateItem</b> method is available for use 
    in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent 
    versions.]

Creates a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> in the 
    <a href="c_gly.htm">cluster</a> and adds it to the 
    <a href="https://msdn.microsoft.com/3164f2ee-7230-4d77-8c7c-cfba3aaee9d4">ClusResTypeResources</a> collection.


## -parameters




### -param bstrResourceName




### -param bstrGroupName




### -param dwFlags




### -param ppClusterResource






#### - lFlag

<b>Long</b> indicating how to create the resource. <i>Flag</i> can 
      be set to one of the following values enumerated from the 
      <a href="https://msdn.microsoft.com/16f5ab58-2507-431a-98f9-bd00a24485ba">CLUSTER_RESOURCE_CREATE_FLAGS</a> 
      enumeration.



#### CLUSTER_RESOURCE_DEFAULT_MONITOR (0)

The <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a> determines the 
        <a href="https://msdn.microsoft.com/caebb47f-c2c5-463e-a957-d9eefc7fc33d">Resource Monitor</a> to which the new resource will be 
        assigned.



#### CLUSTER_RESOURCE_SEPARATE_MONITOR (1)

Causes the Cluster service to create a separate Resource Monitor dedicated exclusively to the new 
        resource.


#### - strGroupName

<b>String</b> containing the name of the 
      <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">group</a> in which to place the new resource.


#### - strResName

<b>String</b> containing the name of the new resource.


## -returns



A <a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a> object that receives the newly 
      added resource.




## -see-also




<a href="https://msdn.microsoft.com/3164f2ee-7230-4d77-8c7c-cfba3aaee9d4">ClusResTypeResources</a>



<a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a>
 

 

