---
UID: NF:msclus.ISClusResource.get_CryptoKeys
title: ISClusResource::get_CryptoKeys
author: windows-sdk-content
description: ClusCryptoKeys collection containing the checkpointed crypto keys for the resource.
old-location: mscs\clusresource_cryptokeys.htm
old-project: MsCS
ms.assetid: 14f75dc0-6d6e-4b70-9481-d00132f2b87b
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ClusResource class [Failover Cluster],CryptoKeys property, ClusResource.CryptoKeys, CryptoKeys property [Failover Cluster], CryptoKeys property [Failover Cluster],ClusResource class, ISClusResource.get_CryptoKeys, ISClusResource::get_CryptoKeys, _wolf_clusresource.cryptokeys, get_CryptoKeys, mscs.clusresource_cryptokeys
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
 - ClusResource.CryptoKeys
 - ISClusResource.get_CryptoKeys
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResource::get_CryptoKeys


## -description


<p class="CCE_Message">[The <b>CryptoKeys</b> 
    property is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Returns a 
    <a href="https://msdn.microsoft.com/0078ba7a-24d7-4de6-af05-f1a03d9deb0a">ClusCryptoKeys</a> collection 
    containing the checkpointed crypto keys for the resource.

This property is read-only.


## -parameters


## -remarks



Use the collection obtained from the 
    <b>CryptoKeys</b> property to add, remove, and list a 
     resource's checkpointed crypto keys.

For more information, see <a href="https://msdn.microsoft.com/6031fe2b-d5cb-477e-9d0f-c8c4a14ce02b">Checkpointing</a>.




## -see-also




<a href="https://msdn.microsoft.com/0078ba7a-24d7-4de6-af05-f1a03d9deb0a">ClusCryptoKeys</a>



<a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a>
 

 

