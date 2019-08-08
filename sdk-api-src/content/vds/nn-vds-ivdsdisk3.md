---
UID: NN:vds.IVdsDisk3
title: IVdsDisk3 (vds.h)
author: windows-sdk-content
description: Provides a method to retrieve property information for a disk, including the disk's location path.
old-location: base\ivdsdisk3.htm
tech.root: VDS
ms.assetid: e3004195-b180-4053-bf91-8f1a0e72f5a6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsDisk3, IVdsDisk3 interface, IVdsDisk3 interface,described, base.ivdsdisk3, vds/IVdsDisk3
ms.topic: interface
f1_keywords:
- vds/IVdsDisk3
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
- IVdsDisk3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsDisk3 interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides a method to retrieve property information for a disk, including the disk's location path.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsDisk3</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsDisk3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsDisk3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsdisk3-getproperties2">GetProperties2</a>
</td>
<td align="left" width="63%">
Returns property 
   information for a disk. This method is identical to the <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsdisk-getproperties">IVdsDisk::GetProperties</a> method, except that it returns a <a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-vds_disk_prop2">VDS_DISK_PROP2</a> structure instead of a <a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-vds_disk_prop">VDS_DISK_PROP</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsdisk3-queryfreeextents">QueryFreeExtents</a>
</td>
<td align="left" width="63%">
Returns the free extents on the disk and aligns them to the specified alignment size.

</td>
</tr>
</table> 

