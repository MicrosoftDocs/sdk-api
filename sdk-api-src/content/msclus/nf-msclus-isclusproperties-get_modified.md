---
UID: NF:msclus.ISClusProperties.get_Modified
title: ISClusProperties::get_Modified
author: windows-sdk-content
description: Indicates whether any properties in the ClusProperties collection have been added or removed, or if any properties have been changed, since the last ClusProperties.Refresh or ClusProperties.SaveChanges operation.
old-location: mscs\clusproperties_modified.htm
old-project: mscs
ms.assetid: 5eaeffda-e2ce-420a-b3f5-da8dfbfdde24
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: ClusProperties collection [Failover Cluster],Modified property, ClusProperties.Modified, ISClusProperties.get_Modified, ISClusProperties::get_Modified, Modified property [Failover Cluster], Modified property [Failover Cluster],ClusProperties collection, _wolf_clusproperties.modified, get_Modified, mscs.clusproperties_modified
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
 - ClusProperties.Modified
 - ISClusProperties.get_Modified
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusProperties::get_Modified


## -description


<p class="CCE_Message">[The <b>Modified</b> 
    property is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Indicates 
    whether any properties in the 
    <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection have been added 
    or removed, or if any properties have been changed, since the last 
    <a href="https://msdn.microsoft.com/900c9401-e8f4-423a-80df-598f5edb2935">ClusProperties.Refresh</a> or 
    <a href="https://msdn.microsoft.com/2792025f-c434-47e0-a5e8-06a992e3a8d2">ClusProperties.SaveChanges</a> 
    operation.

This property is read-only.


## -parameters


## -remarks



To test whether a specific property has been modified, see 
    <a href="https://msdn.microsoft.com/231e9e80-aa4c-4a83-83f6-4276fac4211b">ClusProperty.Modified</a>.




## -see-also




<a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a>



<a href="https://msdn.microsoft.com/900c9401-e8f4-423a-80df-598f5edb2935">ClusProperties.Refresh</a>



<a href="https://msdn.microsoft.com/2792025f-c434-47e0-a5e8-06a992e3a8d2">ClusProperties.SaveChanges</a>
 

 

