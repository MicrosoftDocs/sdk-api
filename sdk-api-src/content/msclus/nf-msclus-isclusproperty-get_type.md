---
UID: NF:msclus.ISClusProperty.get_Type
title: ISClusProperty::get_Type
author: windows-sdk-content
description: Returns or sets the type of a cluster object property.
old-location: mscs\clusproperty_type.htm
old-project: MsCS
ms.assetid: 4cae1bb4-2ca4-4957-b174-1dc07676ce3a
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: CLUSPROP_TYPE_DISK_GUID, CLUSPROP_TYPE_DISK_NUMBER, CLUSPROP_TYPE_DISK_SERIALNUMBER, CLUSPROP_TYPE_DISK_SIZE, CLUSPROP_TYPE_ENDMARK, CLUSPROP_TYPE_LIST_VALUE, CLUSPROP_TYPE_NAME, CLUSPROP_TYPE_PARTITION_INFO, CLUSPROP_TYPE_PARTITION_INFO_EX, CLUSPROP_TYPE_RESCLASS, CLUSPROP_TYPE_SCSI_ADDRESS, CLUSPROP_TYPE_SIGNATURE, CLUSPROP_TYPE_UNKNOWN, CLUSPROP_TYPE_USER, ClusProperty object [Failover Cluster],Type property, ClusProperty.Type, ISClusProperty.get_Type, ISClusProperty::get_Type, Type property [Failover Cluster], Type property [Failover Cluster],ClusProperty object, _wolf_clusproperty.type, get_Type, mscs.clusproperty_type
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
 - kbSyntax
api_type:
 - <TBD>
api_location:
 -
api_name:
 - ClusProperty.Type
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusProperty::get_Type


## -description


<p class="CCE_Message">[The <b>Type</b> property is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Returns or sets the type of a 
    <a href="https://msdn.microsoft.com/ba11ba7a-10f7-4f2c-99cd-d274912ad454">cluster object property</a>.

This property is read-only.


## -parameters


## -remarks



The <b>Type</b> property corresponds to the 
    <b>wType</b> member of a 
    <a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a> union.

For information on making constants defined by the Cluster Automation Server type library (MsClus.tlb) 
    available to scripts, see 
    <a href="https://msdn.microsoft.com/2ca508c9-c34a-4af5-a6c0-3d710171f3df">Creating a Cluster Automation Server Script</a>.




## -see-also




<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/4a10d4f1-2a50-42e7-a143-e9a93d9fcc42">CLUSTER_PROPERTY_TYPE</a>



<a href="https://msdn.microsoft.com/8c285882-915c-45de-9840-cfc5becd55ee">ClusProperty</a>



<a href="https://msdn.microsoft.com/259aba6f-b1a6-422d-859b-8e6c95895ab5">ClusProperty.Format</a>
 

 

