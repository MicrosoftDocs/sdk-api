---
UID: NF:msclus.ISClusResource.get_RegistryKeys
title: ISClusResource::get_RegistryKeys
author: windows-sdk-content
description: Returns a ClusRegistryKeys collection containing the checkpointed registry keys for the resource.
old-location: mscs\clusresource_registrykeys.htm
old-project: MsCS
ms.assetid: 18bb4cfb-cd96-4f43-9cf6-ab06c22d0abf
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ClusResource class [Failover Cluster],RegistryKeys property, ClusResource.RegistryKeys, ISClusResource.get_RegistryKeys, ISClusResource::get_RegistryKeys, RegistryKeys property [Failover Cluster], RegistryKeys property [Failover Cluster],ClusResource class, _wolf_clusresource.registrykeys, get_RegistryKeys, mscs.clusresource_registrykeys
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
 - ClusResource.RegistryKeys
 - ISClusResource.get_RegistryKeys
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResource::get_RegistryKeys


## -description


<p class="CCE_Message">[The <b>RegistryKeys</b> 
    property is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Returns a 
    <a href="https://msdn.microsoft.com/888f70d9-6562-4add-895d-604f22d75307">ClusRegistryKeys</a> collection containing 
    the checkpointed registry keys for the resource.

This property is read-only.


## -parameters


## -remarks



Use the collection obtained from the 
    <b>RegistryKeys</b> property to add, remove, and 
     list a resource's checkpointed keys.

For more information, see <a href="https://msdn.microsoft.com/6031fe2b-d5cb-477e-9d0f-c8c4a14ce02b">Checkpointing</a>.




## -see-also




<a href="https://msdn.microsoft.com/888f70d9-6562-4add-895d-604f22d75307">ClusRegistryKeys</a>



<a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a>



<a href="https://msdn.microsoft.com/14f75dc0-6d6e-4b70-9481-d00132f2b87b">ClusResource.CryptoKeys</a>
 

 

