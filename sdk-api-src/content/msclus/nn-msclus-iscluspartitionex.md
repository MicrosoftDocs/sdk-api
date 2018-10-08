---
UID: NN:msclus.ISClusPartitionEx
title: ISClusPartitionEx
author: windows-sdk-content
description: Provides extended information about a partition on a Physical Disk resource.
old-location: mscs\cluspartitionex.htm
tech.root: MsCS
ms.assetid: 1AFDB11F-1AD4-4B84-82EF-C0CE86D744C1
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ClusPartitionEx, ClusPartitionEx object [Failover Cluster], ClusPartitionEx object [Failover Cluster],described, ISClusPartitionEx, msclus/ClusPartitionEx, mscs.cluspartitionex
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
req.lib: 
req.dll: MsClus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsClus.dll
api_name:
 - ClusPartitionEx
 - ISClusPartitionEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISClusPartitionEx interface


## -description


Provides extended information about a partition on a  <a href="https://msdn.microsoft.com/d42e9bca-3717-44f7-a1b9-dfad1dbddd23">Physical Disk</a> resource.
<ul>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul><h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusPartitionEx</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/D7CC053F-2FA6-4B14-B52A-D3826F88E6F3">DeviceNumber</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the device number of the partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/CFADEA62-389A-4CC7-AC2A-8F80652A3C71">FreeSpace</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the total disk space available to the partition in megabytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/D8E776BD-2880-4F35-95CF-3122E25B9356">PartitionNumber</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the partition number of the partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/B8E131BB-8C66-4542-82FF-01C7C2D2AFE5">TotalSize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the total size of the partition in megabytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6DFFF9D9-0600-4558-9458-44640F405D19">VolumeGuid</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the volume <b>GUID</b> of the partition.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1AFDB11F-1AD4-4B84-82EF-C0CE86D744C1">ClusPartition</a>



<a href="https://msdn.microsoft.com/26d0fd15-9dfd-47cf-baca-87268057f2f3">Disk Management Objects</a>
 

 

