---
UID: NF:msclus.ISClusResGroupResources.DeleteItem
title: ISClusResGroupResources::DeleteItem
author: windows-sdk-content
description: Removes a resource from a ClusResGroupResources collection and deletes it from the cluster.
old-location: mscs\clusresgroupresources_deleteitem.htm
old-project: mscs
ms.assetid: bfd908a3-b968-4729-8ca4-feb687108249
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusResGroupResources class [Failover Cluster],DeleteItem method, ClusResGroupResources.DeleteItem, DeleteItem, DeleteItem method [Failover Cluster], DeleteItem method [Failover Cluster],ClusResGroupResources class, ISClusResGroupResources.DeleteItem, ISClusResGroupResources::DeleteItem, _wolf_clusresgroupresources.deleteitem, mscs.clusresgroupresources_deleteitem
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
 - ClusResGroupResources.DeleteItem
 - ISClusResGroupResources.DeleteItem
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResGroupResources::DeleteItem


## -description


<p class="CCE_Message">[The 
    <b>DeleteItem</b> method is available for use 
    in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent 
    versions.]

Removes a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> from a 
    <a href="https://msdn.microsoft.com/9ea90beb-86ae-4026-94bb-175e593da8fa">ClusResGroupResources</a> collection 
    and deletes it from the <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>.


## -parameters




### -param varIndex

A <b>Variant</b> that identifies a resource in the collection by name or numeric 
      index. Index numbers range from 1 to 
      <a href="https://msdn.microsoft.com/26d90188-e3b7-4546-9305-a2fc50c09c28">ClusResGroupResources.Count</a>.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/9ea90beb-86ae-4026-94bb-175e593da8fa">ClusResGroupResources</a>



<a href="https://msdn.microsoft.com/26d90188-e3b7-4546-9305-a2fc50c09c28">ClusResGroupResources.Count</a>
 

 

