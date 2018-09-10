---
UID: NN:vds.IVdsDisk
title: IVdsDisk
author: windows-sdk-content
description: Provides methods to query and configure basic and dynamic disks.
old-location: base\ivdsdisk.htm
tech.root: VDS
ms.assetid: 0fd6d1d4-daa6-4be3-8749-be98cd7c0288
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IVdsDisk, IVdsDisk interface [VDS], IVdsDisk interface [VDS],described, base.ivdsdisk, vds/IVdsDisk
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsDisk
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsDisk interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods to query and configure basic and dynamic disks.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsDisk</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsDisk</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsDisk</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ee43acd-6dcc-40de-9bb6-de7cfb605f15">ClearFlags</a>
</td>
<td align="left" width="63%">
Clears the flags of a disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38c129cd-8e60-4e4a-b22b-26c69c68fe89">ConvertStyle</a>
</td>
<td align="left" width="63%">
Converts the partition style of an empty disk from one style to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/400fa102-f98a-4bc1-919c-858c135a5b93">GetIdentificationData</a>
</td>
<td align="left" width="63%">
Returns information that uniquely identifies a disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52c7edb5-a92d-423d-8115-e8c3cccd95b5">GetPack</a>
</td>
<td align="left" width="63%">
Returns the disk pack to which the current disk is a member.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2046a26-852d-46b2-b060-98b4a2a92387">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the property details of a disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e7de42f-da7a-41a7-b38e-849ab8d72ab2">QueryExtents</a>
</td>
<td align="left" width="63%">
Returns all extents on a disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ede6a22-b15c-4afd-8d49-c963ea7e2052">SetFlags</a>
</td>
<td align="left" width="63%">
Sets the flags of a disk.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/65e14273-8127-4667-b5c8-362ad54b4782">Disk Object</a>



<a href="https://msdn.microsoft.com/115c1900-5fea-4e39-be3e-b6d04ceb8a58">IVdsPack::QueryDisks</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>



<a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a>
 

 

