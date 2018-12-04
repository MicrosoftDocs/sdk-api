---
UID: NN:vds.IVdsCreatePartitionEx
title: IVdsCreatePartitionEx
author: windows-sdk-content
description: Creates a partition on a basic disk.
old-location: base\ivdscreatepartitionex.htm
tech.root: vds
ms.assetid: aae89a86-35b2-45ab-83f5-9461960876c4
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IVdsCreatePartitionEx, IVdsCreatePartitionEx interface [VDS], IVdsCreatePartitionEx interface [VDS],described, base.ivdscreatepartitionex, vds/IVdsCreatePartitionEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IVdsCreatePartitionEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsCreatePartitionEx interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Creates a partition on a basic disk.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsCreatePartitionEx</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsCreatePartitionEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsCreatePartitionEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9ab5a24-b0b3-41cc-a4bf-3619f156008c">CreatePartitionEx</a>
</td>
<td align="left" width="63%">
Creates a partition on a basic disk.
     

This method supersedes the 
      <a href="https://msdn.microsoft.com/94f80a9f-459f-4f3d-8d85-e5ec7d5734c4">IVdsAdvancedDisk::CreatePartition</a> 
      method.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/94f80a9f-459f-4f3d-8d85-e5ec7d5734c4">IVdsAdvancedDisk::CreatePartition</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

