---
UID: NN:vds.IVdsDiskPartitionMF
title: IVdsDiskPartitionMF (vds.h)
author: windows-sdk-content
description: Provides methods to perform file system management operations on partitions.
old-location: base\ivdsdiskpartitionmf.htm
tech.root: VDS
ms.assetid: 84d0918d-479f-4026-b120-11cc21a43233
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsDiskPartitionMF, IVdsDiskPartitionMF interface, IVdsDiskPartitionMF interface,described, base.ivdsdiskpartitionmf, vds/IVdsDiskPartitionMF
ms.topic: interface
f1_keywords: ["vds/IVdsDiskPartitionMF"]
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IVdsDiskPartitionMF
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsDiskPartitionMF interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods to perform file system management operations on partitions.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsDiskPartitionMF</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsDiskPartitionMF</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsDiskPartitionMF</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsdiskpartitionmf-formatpartitionex">FormatPartitionEx</a>
</td>
<td align="left" width="63%">
Formats an existing OEM, ESP, or unknown partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsdiskpartitionmf-getpartitionfilesystemproperties">GetPartitionFileSystemProperties</a>
</td>
<td align="left" width="63%">
Returns property details about the file system on a partition on the disk at a specified byte offset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsdiskpartitionmf-getpartitionfilesystemtypename">GetPartitionFileSystemTypeName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the file system on a partition on the disk at a specified byte offset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsdiskpartitionmf-querypartitionfilesystemformatsupport">QueryPartitionFileSystemFormatSupport</a>
</td>
<td align="left" width="63%">
Retrieves the properties of the file systems that are supported for formatting a partition on the disk at a specified byte offset.

</td>
</tr>
</table> 

