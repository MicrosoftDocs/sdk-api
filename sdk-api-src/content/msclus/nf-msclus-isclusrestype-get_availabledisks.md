---
UID: NF:msclus.ISClusResType.get_AvailableDisks
title: ISClusResType::get_AvailableDisks
author: windows-sdk-content
description: Returns the collection representing the Physical Disks available to the resource type. A Physical Disk is available if it is cluster-capable and is currently not being used as a resource.
old-location: mscs\clusrestype_availabledisks.htm
old-project: mscs
ms.assetid: fc700541-793b-423b-bea6-ad04deddb16a
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: AvailableDisks property [Failover Cluster], AvailableDisks property [Failover Cluster],ClusResType object, ClusResType object [Failover Cluster],AvailableDisks property, ClusResType.AvailableDisks, ISClusResType.get_AvailableDisks, ISClusResType::get_AvailableDisks, _wolf_clusrestype.availabledisks, get_AvailableDisks, mscs.clusrestype_availabledisks
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
 - ClusResType.AvailableDisks
 - ISClusResType.get_AvailableDisks
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResType::get_AvailableDisks


## -description


<p class="CCE_Message">[The <b>AvailableDisks</b> 
    property is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Returns the 
    collection representing the <a href="https://msdn.microsoft.com/d42e9bca-3717-44f7-a1b9-dfad1dbddd23">Physical Disks</a> available to the 
    resource type. A Physical Disk is available if it is 
    <a href="c_gly.htm">cluster-capable</a> and is currently not being 
    used as a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>.

This property is read-only.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/2823ccb2-5fb2-4e37-b842-340703165871">ClusDisks</a>



<a href="https://msdn.microsoft.com/e4ad6364-f318-47f9-a276-d99c91ffbbb5">ClusResType</a>
 

 

