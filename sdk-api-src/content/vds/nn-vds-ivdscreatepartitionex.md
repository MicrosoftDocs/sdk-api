---
UID: NN:vds.IVdsCreatePartitionEx
title: IVdsCreatePartitionEx (vds.h)
author: windows-sdk-content
description: Creates a partition on a basic disk.
old-location: base\ivdscreatepartitionex.htm
tech.root: VDS
ms.assetid: aae89a86-35b2-45ab-83f5-9461960876c4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsCreatePartitionEx, IVdsCreatePartitionEx interface [VDS], IVdsCreatePartitionEx interface [VDS],described, base.ivdscreatepartitionex, vds/IVdsCreatePartitionEx
ms.topic: interface
f1_keywords: 
 - "vds/IVdsCreatePartitionEx"
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
ms.custom: 19H1
---

# IVdsCreatePartitionEx interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Creates a partition on a basic disk.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsCreatePartitionEx</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsCreatePartitionEx</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdscreatepartitionex-createpartitionex">CreatePartitionEx</a>
</td>
<td align="left" width="63%">
Creates a partition on a basic disk.
     

This method supersedes the 
      <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-createpartition">IVdsAdvancedDisk::CreatePartition</a> 
      method.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-createpartition">IVdsAdvancedDisk::CreatePartition</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

