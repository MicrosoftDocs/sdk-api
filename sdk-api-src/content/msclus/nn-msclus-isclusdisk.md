---
UID: NN:msclus.ISClusDisk
title: ISClusDisk
author: windows-driver-content
description: Provides access to identification and configuration data about a Physical Disk.
old-location: mscs\clusdisk_object.htm
old-project: MsCS
ms.assetid: 6433d55f-f97a-4027-ba2a-7102b4cf33ae
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: ClusDisk, ClusDisk object [Failover Cluster], ClusDisk object [Failover Cluster],described, ISClusDisk, _wolf_clusdisk_object, msclus/ClusDisk, mscs.clusdisk_object
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CLUS_GROUP_START_SETTING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsClus.dll
api_name:
-	ClusDisk
-	ISClusDisk
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusDisk interface


## -description


<p class="CCE_Message">[The <b>ClusDisk</b> object is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Provides access to 
    identification and configuration data about a 
    <a href="https://msdn.microsoft.com/d42e9bca-3717-44f7-a1b9-dfad1dbddd23">Physical Disk</a>.


## -remarks



A <b>ClusDisk</b> object is obtained from 
    <a href="https://msdn.microsoft.com/4199a230-1e1d-45d5-b93b-5f12b58c8f35">ClusDisks.Item</a> or 
    <a href="https://msdn.microsoft.com/4f85a491-3cb7-409a-a7fb-9fc0f896e787">ClusResource.Disk</a>.



