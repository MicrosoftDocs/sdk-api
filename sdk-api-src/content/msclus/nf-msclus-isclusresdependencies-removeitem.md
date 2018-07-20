---
UID: NF:msclus.ISClusResDependencies.RemoveItem
title: ISClusResDependencies::RemoveItem
author: windows-sdk-content
description: Removes a resource from the dependency collection but does not delete it from the cluster.
old-location: mscs\clusresdependencies_removeitem.htm
old-project: mscs
ms.assetid: 904556e2-7d0b-4c03-8cf5-795342263045
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: ClusResDependencies class [Failover Cluster],RemoveItem method, ClusResDependencies.RemoveItem, ISClusResDependencies.RemoveItem, ISClusResDependencies::RemoveItem, RemoveItem, RemoveItem method [Failover Cluster], RemoveItem method [Failover Cluster],ClusResDependencies class, _wolf_clusresdependencies.removeitem, mscs.clusresdependencies_removeitem
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
 - ClusResDependencies.RemoveItem
 - ISClusResDependencies.RemoveItem
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResDependencies::RemoveItem


## -description


<p class="CCE_Message">[The <b>RemoveItem</b> 
    method is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Removes a 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> from the 
    <a href="d_gly.htm">dependency</a> collection but does not delete it from the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.


## -parameters




### -param varIndex

A <b>Variant</b> that identifies a resource in the collection by name or numeric 
      index. Index numbers range from 1 to 
      <a href="https://msdn.microsoft.com/c946eda8-e6f5-4e5b-9512-31d718820edc">ClusResDependencies.Count</a>.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/10695840-38ec-4614-8bbd-5772a53dea4b">ClusResDependencies</a>



<a href="https://msdn.microsoft.com/c946eda8-e6f5-4e5b-9512-31d718820edc">ClusResDependencies.Count</a>
 

 

