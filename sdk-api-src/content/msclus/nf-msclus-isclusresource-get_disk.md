---
UID: NF:msclus.ISClusResource.get_Disk
title: ISClusResource::get_Disk
author: windows-sdk-content
description: ClusDisk object providing access to information about the disk.
old-location: mscs\clusresource_disk.htm
old-project: mscs
ms.assetid: 4f85a491-3cb7-409a-a7fb-9fc0f896e787
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusResource class [Failover Cluster],Disk property, ClusResource.Disk, Disk property [Failover Cluster], Disk property [Failover Cluster],ClusResource class, ISClusResource.get_Disk, ISClusResource::get_Disk, _wolf_clusresource.disk, get_Disk, mscs.clusresource_disk
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msclus.h
req.include-header: 
req.redist: 
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
 - ClusResource.Disk
 - ISClusResource.get_Disk
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResource::get_Disk


## -description


<p class="CCE_Message">[The <b>Disk</b> property is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

For <a href="https://msdn.microsoft.com/d42e9bca-3717-44f7-a1b9-dfad1dbddd23">Physical Disk</a>, the 
    <b>Disk</b> property returns a 
    <a href="https://msdn.microsoft.com/6433d55f-f97a-4027-ba2a-7102b4cf33ae">ClusDisk</a> object providing access to 
    information about the disk. For other types of resources, the 
    <b>Disk</b> property returns nothing.

This property is read-only.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/6433d55f-f97a-4027-ba2a-7102b4cf33ae">ClusDisk</a>



<a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a>
 

 

