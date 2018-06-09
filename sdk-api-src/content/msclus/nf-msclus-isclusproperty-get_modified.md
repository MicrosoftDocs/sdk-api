---
UID: NF:msclus.ISClusProperty.get_Modified
title: ISClusProperty::get_Modified
author: windows-sdk-content
description: Indicates whether the value of the property has changed since the last ClusProperties.Refresh or ClusProperties.SaveChanges operation.
old-location: mscs\clusproperty_modified.htm
old-project: MsCS
ms.assetid: 231e9e80-aa4c-4a83-83f6-4276fac4211b
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ClusProperty object [Failover Cluster],Modified property, ClusProperty.Modified, ISClusProperty.get_Modified, ISClusProperty::get_Modified, Modified property [Failover Cluster], Modified property [Failover Cluster],ClusProperty object, _wolf_clusproperty.modified, get_Modified, mscs.clusproperty_modified
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
 - ClusProperty.Modified
 - ISClusProperty.get_Modified
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusProperty::get_Modified


## -description


<p class="CCE_Message">[The <b>Modified</b> property 
    is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable 
    in subsequent versions.]

Indicates 
    whether the value of the property has changed since the last 
    <a href="https://msdn.microsoft.com/900c9401-e8f4-423a-80df-598f5edb2935">ClusProperties.Refresh</a> or 
    <a href="https://msdn.microsoft.com/2792025f-c434-47e0-a5e8-06a992e3a8d2">ClusProperties.SaveChanges</a> 
    operation.

This property is read-only.


## -parameters


## -remarks



A <a href="https://msdn.microsoft.com/8c285882-915c-45de-9840-cfc5becd55ee">ClusProperty</a> object operates on a local copy 
    of cluster property data. Changes made to the local copy of the data do not take effect in the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> until the parent 
    <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection invokes the 
    <a href="https://msdn.microsoft.com/2792025f-c434-47e0-a5e8-06a992e3a8d2">ClusProperties.SaveChanges</a> 
    method. Any change to the local copy of the property value causes 
    <b>Modified</b> to return 
    <b>VARIANT_TRUE</b>.




## -see-also




<b>ClusProperties</b>



<a href="https://msdn.microsoft.com/900c9401-e8f4-423a-80df-598f5edb2935">ClusProperties.Refresh</a>



<a href="https://msdn.microsoft.com/2792025f-c434-47e0-a5e8-06a992e3a8d2">ClusProperties.SaveChanges</a>



<a href="https://msdn.microsoft.com/8c285882-915c-45de-9840-cfc5becd55ee">ClusProperty</a>
 

 

