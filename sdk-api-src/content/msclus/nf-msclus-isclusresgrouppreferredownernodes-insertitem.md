---
UID: NF:msclus.ISClusResGroupPreferredOwnerNodes.InsertItem
title: ISClusResGroupPreferredOwnerNodes::InsertItem
author: windows-sdk-content
description: Adds a node to the ClusResGroupPreferredOwnerNodes collection.
old-location: mscs\clusresgrouppreferredownernodes_insertitem.htm
old-project: mscs
ms.assetid: ae234397-a592-41a3-a30d-cb4b6450e332
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusResGroupPreferredOwnerNodes class [Failover Cluster],InsertItem method, ClusResGroupPreferredOwnerNodes.InsertItem, ISClusResGroupPreferredOwnerNodes.InsertItem, ISClusResGroupPreferredOwnerNodes::InsertItem, InsertItem, InsertItem method [Failover Cluster], InsertItem method [Failover Cluster],ClusResGroupPreferredOwnerNodes class, _wolf_clusresgrouppreferredownernodes.insertitem, mscs.clusresgrouppreferredownernodes_insertitem
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
 - ClusResGroupPreferredOwnerNodes.InsertItem
 - ISClusResGroupPreferredOwnerNodes.InsertItem
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResGroupPreferredOwnerNodes::InsertItem


## -description


<p class="CCE_Message">[The 
    <b>InsertItem</b> method is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Adds a <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> to the 
    <a href="https://msdn.microsoft.com/3425825e-890c-4d3d-919e-a66963e1fc55">ClusResGroupPreferredOwnerNodes</a> 
    collection.


## -parameters




### -param pNode




### -param nPosition






#### - objNode

A <a href="https://msdn.microsoft.com/b164f5a6-13f1-4eff-a2f9-805b60138dd1">ClusNode</a> object to be added to the 
      collection.


#### - lPosition

Optional. <b>Long</b> that identifies the location within the collection to add the 
      new node. Highly preferred, high-priority nodes have low position values (that is, they occur first in the 
      list).


## -returns



This method does not return a value.




## -remarks



Adding a node to a group's 
    <a href="https://msdn.microsoft.com/3425825e-890c-4d3d-919e-a66963e1fc55">ClusResGroupPreferredOwnerNodes</a> 
    collection means that the node is listed as a 
    <a href="p_gly.htm">preferred owner</a> node for the group. Use 
    <i>lPosition</i> to specify an order of preference, with low values corresponding to highly 
    preferred, high-priority nodes.

To add a node to the end of the list, use the 
    <a href="https://msdn.microsoft.com/001e2766-d489-4406-b11e-c19c6426dfd4">ClusResGroupPreferredOwnerNodes.AddItem</a> 
    method.




## -see-also




<a href="https://msdn.microsoft.com/b164f5a6-13f1-4eff-a2f9-805b60138dd1">ClusNode</a>



<a href="https://msdn.microsoft.com/3425825e-890c-4d3d-919e-a66963e1fc55">ClusResGroupPreferredOwnerNodes</a>



<a href="https://msdn.microsoft.com/001e2766-d489-4406-b11e-c19c6426dfd4">ClusResGroupPreferredOwnerNodes.AddItem</a>
 

 

