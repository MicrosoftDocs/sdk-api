---
UID: NF:msclus.ISClusResDependents.RemoveItem
title: ISClusResDependents::RemoveItem
author: windows-sdk-content
description: Removes a resource from the ClusResDependents collection but does not delete it from the cluster.
old-location: mscs\clusresdependents_removeitem.htm
old-project: mscs
ms.assetid: 70cee9b9-4d21-4237-8262-211e1b87923f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusResDependents class [Failover Cluster],RemoveItem method, ClusResDependents.RemoveItem, ISClusResDependents.RemoveItem, ISClusResDependents::RemoveItem, RemoveItem, RemoveItem method [Failover Cluster], RemoveItem method [Failover Cluster],ClusResDependents class, _wolf_clusresdependents.removeitem, mscs.clusresdependents_removeitem
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
 - ClusResDependents.RemoveItem
 - ISClusResDependents.RemoveItem
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResDependents::RemoveItem


## -description


<p class="CCE_Message">[The <b>RemoveItem</b> 
    method is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Removes a 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> from the 
    <a href="https://msdn.microsoft.com/4e1f47fa-e240-4fdb-b736-9b2e64828eb0">ClusResDependents</a> collection but does 
    not delete it from the <a href="c_gly.htm">cluster</a>.


## -parameters




### -param varIndex

A <b>Variant</b> that identifies a resource in the collection by name or numeric 
      index. Index numbers range from 1 to 
      <a href="https://msdn.microsoft.com/ab02c5ba-d63f-4eab-bad4-804760a8a40b">ClusResDependents.Count</a>.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/4e1f47fa-e240-4fdb-b736-9b2e64828eb0">ClusResDependents</a>



<a href="https://msdn.microsoft.com/ab02c5ba-d63f-4eab-bad4-804760a8a40b">ClusResDependents.Count</a>
 

 

