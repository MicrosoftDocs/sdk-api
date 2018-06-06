---
UID: NN:vds.IVdsDiskPartitionMF
title: IVdsDiskPartitionMF
author: windows-sdk-content
description: Provides methods to perform file system management operations on partitions.
old-location: base\ivdsdiskpartitionmf.htm
old-project: VDS
ms.assetid: 84d0918d-479f-4026-b120-11cc21a43233
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IVdsDiskPartitionMF, IVdsDiskPartitionMF interface, IVdsDiskPartitionMF interface,described, base.ivdsdiskpartitionmf, vds/IVdsDiskPartitionMF
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: VDS_VOLUME_TYPE
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsDiskPartitionMF interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods to perform file system management operations on partitions.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsDiskPartitionMF</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsDiskPartitionMF</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/82ab6b70-bfa3-4246-aa82-05c6c3b3cbe9">FormatPartitionEx</a>
</td>
<td align="left" width="63%">
Formats an existing OEM, ESP, or unknown partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b49ffba-00df-4d8f-a90f-5e26a5c898dd">GetPartitionFileSystemProperties</a>
</td>
<td align="left" width="63%">
Returns property details about the file system on a partition on the disk at a specified byte offset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad2f8c5b-6a85-437a-bb51-0c4552a015b2">GetPartitionFileSystemTypeName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the file system on a partition on the disk at a specified byte offset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ee61c81-28d2-43d8-8444-a62dc025aed0">QueryPartitionFileSystemFormatSupport</a>
</td>
<td align="left" width="63%">
Retrieves the properties of the file systems that are supported for formatting a partition on the disk at a specified byte offset.

</td>
</tr>
</table> 

