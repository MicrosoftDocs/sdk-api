---
UID: NF:msclus.ISClusResTypes.DeleteItem
title: ISClusResTypes::DeleteItem
author: windows-sdk-content
description: Deletes a resource type from the cluster and removes it from the ClusResTypes collection.
old-location: mscs\clusrestypes_deleteitem.htm
old-project: mscs
ms.assetid: 0a528b4e-8d6d-434b-b005-ca732c72c7a3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusResTypes collection [Failover Cluster],DeleteItem method, ClusResTypes.DeleteItem, DeleteItem, DeleteItem method [Failover Cluster], DeleteItem method [Failover Cluster],ClusResTypes collection, ISClusResTypes.DeleteItem, ISClusResTypes::DeleteItem, _wolf_clusrestypes.deleteitem, mscs.clusrestypes_deleteitem
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
 - ClusResTypes.DeleteItem
 - ISClusResTypes.DeleteItem
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResTypes::DeleteItem


## -description


<p class="CCE_Message">[The <b>DeleteItem</b> method 
    is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable 
    in subsequent versions.]

Deletes a 
    <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type</a> from the 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a> and removes it from the 
    <a href="https://msdn.microsoft.com/614d3ed6-255f-46ed-9354-7a73a21cac87">ClusResTypes</a> collection.


## -parameters




### -param varIndex

Integer that identifies an object in the collection by name or numeric index.


## -returns



This method does not return a value.




## -remarks



If there are any resources of the specified type present in the cluster, the 
    <b>DeleteItem</b> method fails for that resource type. 
    In other words, you cannot delete a resource type if there are resources of that type present in the cluster.




## -see-also




<a href="https://msdn.microsoft.com/614d3ed6-255f-46ed-9354-7a73a21cac87">ClusResTypes</a>
 

 

