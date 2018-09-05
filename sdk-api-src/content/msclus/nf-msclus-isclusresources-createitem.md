---
UID: NF:msclus.ISClusResources.CreateItem
title: ISClusResources::CreateItem
author: windows-sdk-content
description: Creates a resource and adds it to a ClusResources collection.
old-location: mscs\clusresources_createitem.htm
old-project: mscs
ms.assetid: 3ff2d33b-08aa-445b-930e-7fbe589f6269
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CLUSTER_RESOURCE_DEFAULT_MONITOR, CLUSTER_RESOURCE_SEPARATE_MONITOR, ClusResources collection [Failover Cluster],CreateItem method, ClusResources.CreateItem, CreateItem, CreateItem method [Failover Cluster], CreateItem method [Failover Cluster],ClusResources collection, ISClusResources.CreateItem, ISClusResources::CreateItem, _wolf_clusresources.createitem, mscs.clusresources_createitem
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
 - ClusResources.CreateItem
 - ISClusResources.CreateItem
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResources::CreateItem


## -description


<p class="CCE_Message">[The <b>CreateItem</b> 
    method is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Creates a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> and adds it to a 
    <a href="https://msdn.microsoft.com/56dd53e7-7e2e-481f-b343-da51c7c52553">ClusResources</a> collection.


## -parameters




### -param bstrResourceName




### -param bstrResourceType




### -param bstrGroupName




### -param dwFlags




### -param ppClusterResource






#### - lFlag

Value indicating how to create the resource. <i>lFlag</i> can be set to one of these 
      values enumerated from the 
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

<b>String</b> containing the name of the group to which the new resource will 
      belong.


#### - strResourceName

<b>String</b> containing the name of the resource to create.


#### - strResourceType

<b>String</b> specifying the type of resource to create.


## -returns



Object that receives contains the new 
      <a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a> object representing the new 
      resource.




## -remarks



For information on making constants defined by the Cluster Automation Server type library (MsClus.tlb) 
    available to scripts, see 
    <a href="https://msdn.microsoft.com/2ca508c9-c34a-4af5-a6c0-3d710171f3df">Creating a Cluster Automation Server Script</a>.




## -see-also




<a href="https://msdn.microsoft.com/16f5ab58-2507-431a-98f9-bd00a24485ba">CLUSTER_RESOURCE_CREATE_FLAGS</a>



<a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a>



<a href="https://msdn.microsoft.com/56dd53e7-7e2e-481f-b343-da51c7c52553">ClusResources</a>
 

 

