---
UID: NF:msclus.ISClusResGroupPreferredOwnerNodes.RemoveItem
title: ISClusResGroupPreferredOwnerNodes::RemoveItem
author: windows-sdk-content
description: Removes a node from the ClusResGroupPreferredOwnerNodes collection.
old-location: mscs\clusresgrouppreferredownernodes_removeitem.htm
old-project: MsCS
ms.assetid: 9126b3ae-4dd3-402a-bda9-ce2d3ded8b36
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ClusResGroupPreferredOwnerNodes class [Failover Cluster],RemoveItem method, ClusResGroupPreferredOwnerNodes.RemoveItem, ISClusResGroupPreferredOwnerNodes.RemoveItem, ISClusResGroupPreferredOwnerNodes::RemoveItem, RemoveItem, RemoveItem method [Failover Cluster], RemoveItem method [Failover Cluster],ClusResGroupPreferredOwnerNodes class, _wolf_clusresgrouppreferredownernodes.removeitem, mscs.clusresgrouppreferredownernodes_removeitem
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
 - ClusResGroupPreferredOwnerNodes.RemoveItem
 - ISClusResGroupPreferredOwnerNodes.RemoveItem
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResGroupPreferredOwnerNodes::RemoveItem


## -description


<p class="CCE_Message">[The 
    <b>RemoveItem</b> method is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Removes a <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> from the 
    <a href="https://msdn.microsoft.com/3425825e-890c-4d3d-919e-a66963e1fc55">ClusResGroupPreferredOwnerNodes</a> 
    collection.


## -parameters




### -param varIndex

A <b>Variant</b> identifying the node to be removed either by name or numeric 
      index.


## -returns



This method does not return a value.




## -remarks



Removing a node from a <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">group's</a>
<a href="https://msdn.microsoft.com/3425825e-890c-4d3d-919e-a66963e1fc55">ClusResGroupPreferredOwnerNodes</a> 
    collection removes the node from the group's 
    <a href="https://msdn.microsoft.com/library/ms682858(v=VS.85).aspx">preferred owners</a> list.




## -see-also




<a href="https://msdn.microsoft.com/3425825e-890c-4d3d-919e-a66963e1fc55">ClusResGroupPreferredOwnerNodes</a>
 

 

