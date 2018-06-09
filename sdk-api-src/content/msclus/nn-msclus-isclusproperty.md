---
UID: NN:msclus.ISClusProperty
title: ISClusProperty
author: windows-sdk-content
description: Represents a single property within a ClusProperties collection.
old-location: mscs\clusproperty_object.htm
old-project: MsCS
ms.assetid: 8c285882-915c-45de-9840-cfc5becd55ee
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ClusProperty, ClusProperty object [Failover Cluster], ClusProperty object [Failover Cluster],described, ISClusProperty, _wolf_clusproperty_object, msclus/ClusProperty, mscs.clusproperty_object
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ClusProperty
 - ISClusProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusProperty interface


## -description


<p class="CCE_Message">[The <b>ClusProperty</b> object 
    is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable 
    in subsequent versions.]

Represents a 
    single property within a <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> 
    collection.


## -remarks



A <b>ClusProperty</b> object contains a local copy of 
    real property data stored in the cluster database. Changes to the 
    <b>ClusProperty</b> object do not take effect in the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> until the parent 
    <a href="https://msdn.microsoft.com/2792025f-c434-47e0-a5e8-06a992e3a8d2">ClusProperties.SaveChanges</a> method 
    is invoked. Similarly, changes to the cluster database are not reflected in the object until the 
    <a href="https://msdn.microsoft.com/900c9401-e8f4-423a-80df-598f5edb2935">ClusProperties.Refresh</a> method is 
    called.

A <b>ClusProperty</b> object can only be obtained from 
    a <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> 
    collection.




## -see-also




<a href="https://msdn.microsoft.com/386405da-1f57-46a2-b913-b946d7574ede">Property Management Objects</a>
 

 

