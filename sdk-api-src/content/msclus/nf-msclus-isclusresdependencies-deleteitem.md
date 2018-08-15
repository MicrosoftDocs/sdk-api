---
UID: NF:msclus.ISClusResDependencies.DeleteItem
title: ISClusResDependencies::DeleteItem
author: windows-sdk-content
description: Removes a resource from the dependency collection and deletes the resource from the cluster.
old-location: mscs\clusresdependencies_deleteitem.htm
old-project: mscs
ms.assetid: 01706fd2-48cc-4d98-a296-58caecc5857b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusResDependencies class [Failover Cluster],DeleteItem method, ClusResDependencies.DeleteItem, DeleteItem, DeleteItem method [Failover Cluster], DeleteItem method [Failover Cluster],ClusResDependencies class, ISClusResDependencies.DeleteItem, ISClusResDependencies::DeleteItem, _wolf_clusresdependencies.deleteitem, mscs.clusresdependencies_deleteitem
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
 - ClusResDependencies.DeleteItem
 - ISClusResDependencies.DeleteItem
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResDependencies::DeleteItem


## -description


<p class="CCE_Message">[The <b>DeleteItem</b> 
    method is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Removes 
    a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> from the 
    <a href="d_gly.htm">dependency</a> collection and deletes the resource from the 
    <a href="c_gly.htm">cluster</a>.


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
 

 

