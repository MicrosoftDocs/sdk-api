---
UID: NF:msclus.ISClusProperty.get_Name
title: ISClusProperty::get_Name
author: windows-sdk-content
description: Name of a cluster object property.
old-location: mscs\clusproperty_name.htm
old-project: MsCS
ms.assetid: b2d2f8b2-5bfe-4ed9-a746-79490806d85e
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ClusProperty object [Failover Cluster],Name property, ClusProperty.Name, ISClusProperty.get_Name, ISClusProperty::get_Name, Name property [Failover Cluster], Name property [Failover Cluster],ClusProperty object, _wolf_clusproperty.name, get_Name, mscs.clusproperty_name
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
 - ClusProperty.Name
 - ISClusProperty.get_Name
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusProperty::get_Name


## -description


<p class="CCE_Message">[The <b>Name</b> property is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable 
    in subsequent versions.]

Returns the name of a 
    <a href="https://msdn.microsoft.com/ba11ba7a-10f7-4f2c-99cd-d274912ad454">cluster object property</a>.

This property is read-only.


## -parameters


## -remarks



The <b>Name</b> returned depends on the specific 
    <a href="https://msdn.microsoft.com/8c285882-915c-45de-9840-cfc5becd55ee">ClusProperty</a> object and the associated 
    <a href="https://msdn.microsoft.com/4a765dce-c823-4a79-8608-ff41feec8a39">cluster object</a>. For detailed information about the 
    properties associated with cluster objects, see 
    <a href="https://msdn.microsoft.com/ba11ba7a-10f7-4f2c-99cd-d274912ad454">Cluster Object Properties</a>.




## -see-also




<a href="https://msdn.microsoft.com/8c285882-915c-45de-9840-cfc5becd55ee">ClusProperty</a>
 

 

