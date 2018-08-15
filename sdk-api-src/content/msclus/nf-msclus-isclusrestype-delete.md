---
UID: NF:msclus.ISClusResType.Delete
title: ISClusResType::Delete
author: windows-sdk-content
description: Deletes the resource type from the cluster and unregisters the type with the Cluster service.
old-location: mscs\clusrestype_delete.htm
old-project: mscs
ms.assetid: b71789a5-7e88-418e-acf4-f28f60b03e3a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusResType object [Failover Cluster],Delete method, ClusResType.Delete, Delete, Delete method [Failover Cluster], Delete method [Failover Cluster],ClusResType object, ISClusResType.Delete, ISClusResType::Delete, _wolf_clusrestype.delete, mscs.clusrestype_delete
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
 - ClusResType.Delete
 - ISClusResType.Delete
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResType::Delete


## -description


<p class="CCE_Message">[The <b>Delete</b> object is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Deletes the 
    <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type</a> from the 
    <a href="c_gly.htm">cluster</a> and unregisters the type with the 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">Cluster service</a>.


## -parameters






## -returns



This method does not return a value.




## -remarks



This method will fail if any resources of the specified type exist in the cluster. Once a resource type is 
    deleted, no resources of that type can be created in the cluster until the resource type is re-created.




## -see-also




<a href="https://msdn.microsoft.com/e4ad6364-f318-47f9-a276-d99c91ffbbb5">ClusResType</a>
 

 

