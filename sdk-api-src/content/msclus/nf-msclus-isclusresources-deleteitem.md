---
UID: NF:msclus.ISClusResources.DeleteItem
title: ISClusResources::DeleteItem
author: windows-sdk-content
description: Deletes a resource from the cluster and removes it from a ClusResources collection.
old-location: mscs\clusresources_deleteitem.htm
old-project: mscs
ms.assetid: 200783e7-a2e6-489f-8271-36b8b6496b8e
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: ClusResources collection [Failover Cluster],DeleteItem method, ClusResources.DeleteItem, DeleteItem, DeleteItem method [Failover Cluster], DeleteItem method [Failover Cluster],ClusResources collection, ISClusResources.DeleteItem, ISClusResources::DeleteItem, _wolf_clusresources.deleteitem, mscs.clusresources_deleteitem
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
 - ClusResources.DeleteItem
 - ISClusResources.DeleteItem
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResources::DeleteItem


## -description


<p class="CCE_Message">[The <b>DeleteItem</b> 
    method is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Deletes a 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> from the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> and removes it from a 
    <a href="https://msdn.microsoft.com/56dd53e7-7e2e-481f-b343-da51c7c52553">ClusResources</a> collection.


## -parameters




### -param varIndex

Integer that identifies an object in the collection by name or numeric index. Index numbers range from 1 to 
      <a href="https://msdn.microsoft.com/6c9ff4bd-8474-4e88-b70e-bc9e661382ab">ClusResources.Count</a>.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/56dd53e7-7e2e-481f-b343-da51c7c52553">ClusResources</a>



<a href="https://msdn.microsoft.com/6c9ff4bd-8474-4e88-b70e-bc9e661382ab">ClusResources.Count</a>
 

 

