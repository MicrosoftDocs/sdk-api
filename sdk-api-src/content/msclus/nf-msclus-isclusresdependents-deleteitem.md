---
UID: NF:msclus.ISClusResDependents.DeleteItem
title: ISClusResDependents::DeleteItem
author: windows-sdk-content
description: Removes a resource from the ClusResDependents collection and deletes the resource from the cluster.
old-location: mscs\clusresdependents_deleteitem.htm
old-project: mscs
ms.assetid: c737bed3-3af0-475e-8e4e-cb7d1ce99792
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: ClusResDependents class [Failover Cluster],DeleteItem method, ClusResDependents.DeleteItem, DeleteItem, DeleteItem method [Failover Cluster], DeleteItem method [Failover Cluster],ClusResDependents class, ISClusResDependents.DeleteItem, ISClusResDependents::DeleteItem, _wolf_clusresdependents.deleteitem, mscs.clusresdependents_deleteitem
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
 - ClusResDependents.DeleteItem
 - ISClusResDependents.DeleteItem
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResDependents::DeleteItem


## -description


<p class="CCE_Message">[The <b>DeleteItem</b> 
    method is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Removes a 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> from the 
    <a href="https://msdn.microsoft.com/4e1f47fa-e240-4fdb-b736-9b2e64828eb0">ClusResDependents</a> collection and 
    deletes the resource from the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.


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
 

 

