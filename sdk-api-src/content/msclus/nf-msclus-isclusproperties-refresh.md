---
UID: NF:msclus.ISClusProperties.Refresh
title: ISClusProperties::Refresh
author: windows-sdk-content
description: Reads the cluster database and updates the data in the ClusProperties collection to reflect the current cluster data.
old-location: mscs\clusproperties_refresh.htm
old-project: MsCS
ms.assetid: 900c9401-e8f4-423a-80df-598f5edb2935
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ClusProperties collection [Failover Cluster],Refresh method, ClusProperties.Refresh, ISClusProperties.Refresh, ISClusProperties::Refresh, Refresh, Refresh method [Failover Cluster], Refresh method [Failover Cluster],ClusProperties collection, _wolf_clusproperties.refresh, mscs.clusproperties_refresh
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
 - ClusProperties.Refresh
 - ISClusProperties.Refresh
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusProperties::Refresh


## -description


<p class="CCE_Message">[The <b>Refresh</b> method is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Reads the 
    <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> and updates the data in the 
    <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection to reflect the 
    current <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> data.


## -parameters






## -returns



This method does not return a value.




## -remarks



A <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> 
    collection contains a local copy of property data. The 
    <b>Refresh</b> method updates the local copy with the 
    current property data from the cluster. Any unsaved changes in the collection will be overwritten.

The <b>Refresh</b> method causes the 
    <a href="https://msdn.microsoft.com/5eaeffda-e2ce-420a-b3f5-da8dfbfdde24">ClusProperties.Modified</a> property to return 
    <b>VARIANT_FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a>
 

 

