---
UID: NF:msclus.ISClusRegistryKeys.RemoveItem
title: ISClusRegistryKeys::RemoveItem
author: windows-sdk-content
description: Deletes a registry key from a ClusRegistryKeys collection.
old-location: mscs\clusregistrykeys_removeitem.htm
old-project: mscs
ms.assetid: 32b2eef7-40b1-4bfe-9f28-43831006d4cb
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: ClusRegistryKeys class [Failover Cluster],RemoveItem method, ClusRegistryKeys.RemoveItem, ISClusRegistryKeys.RemoveItem, ISClusRegistryKeys::RemoveItem, RemoveItem, RemoveItem method [Failover Cluster], RemoveItem method [Failover Cluster],ClusRegistryKeys class, _wolf_clusregistrykeys.removeitem, mscs.clusregistrykeys_removeitem
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
 - ClusRegistryKeys.RemoveItem
 - ISClusRegistryKeys.RemoveItem
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusRegistryKeys::RemoveItem


## -description


<p class="CCE_Message">[The <b>RemoveItem</b> 
    method is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Deletes a 
    registry key from a <a href="https://msdn.microsoft.com/888f70d9-6562-4add-895d-604f22d75307">ClusRegistryKeys</a> 
    collection.


## -parameters




### -param varIndex

A <b>Variant</b> specifying the key to remove by name or by numeric index.


## -returns



This method does not return a value.




## -remarks



Use the <b>RemoveItem</b> method to remove a 
    registry key from a resource's list of checkpointed registry keys.

For more information on checkpoints, see 
    <a href="https://msdn.microsoft.com/6031fe2b-d5cb-477e-9d0f-c8c4a14ce02b">Checkpointing</a>.




## -see-also




<a href="https://msdn.microsoft.com/888f70d9-6562-4add-895d-604f22d75307">ClusRegistryKeys</a>
 

 

