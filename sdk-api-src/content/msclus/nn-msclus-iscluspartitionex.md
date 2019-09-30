---
UID: NN:msclus.ISClusPartitionEx
title: ISClusPartitionEx (msclus.h)
author: windows-sdk-content
description: Provides extended information about a partition on a Physical Disk resource.
old-location: mscs\cluspartitionex.htm
tech.root: MsCS
ms.assetid: 1AFDB11F-1AD4-4B84-82EF-C0CE86D744C1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ClusPartitionEx, ClusPartitionEx object [Failover Cluster], ClusPartitionEx object [Failover Cluster],described, ISClusPartitionEx, msclus/ClusPartitionEx, mscs.cluspartitionex
ms.topic: interface
f1_keywords: 
 - "msclus/ClusPartitionEx"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISClusPartitionEx interface


## -description


Provides extended information about a partition on a  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/physical-disk">Physical Disk</a> resource.
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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluspartitionex-devicenumber">DeviceNumber</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluspartitionex-freespace">FreeSpace</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluspartitionex-partitionnumber">PartitionNumber</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluspartitionex-totalsize">TotalSize</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluspartitionex-volumeguid">VolumeGuid</a>


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msclus/nn-msclus-iscluspartitionex">ClusPartition</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/disk-management-objects">Disk Management Objects</a>
 

 

