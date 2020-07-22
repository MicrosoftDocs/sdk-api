---
UID: NN:vds.IVdsDisk
title: IVdsDisk (vds.h)
description: Provides methods to query and configure basic and dynamic disks.
helpviewer_keywords: ["IVdsDisk","IVdsDisk interface [VDS]","IVdsDisk interface [VDS]","described","base.ivdsdisk","vds/IVdsDisk"]
old-location: base\ivdsdisk.htm
tech.root: base
ms.assetid: 0fd6d1d4-daa6-4be3-8749-be98cd7c0288
ms.date: 12/05/2018
ms.keywords: IVdsDisk, IVdsDisk interface [VDS], IVdsDisk interface [VDS],described, base.ivdsdisk, vds/IVdsDisk
f1_keywords:
- vds/IVdsDisk
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsDisk interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods to query and configure basic and dynamic disks.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsDisk</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsDisk</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsdisk-clearflags">ClearFlags</a>
</td>
<td align="left" width="63%">
Clears the flags of a disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsdisk-convertstyle">ConvertStyle</a>
</td>
<td align="left" width="63%">
Converts the partition style of an empty disk from one style to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsdisk-getidentificationdata">GetIdentificationData</a>
</td>
<td align="left" width="63%">
Returns information that uniquely identifies a disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsdisk-getpack">GetPack</a>
</td>
<td align="left" width="63%">
Returns the disk pack to which the current disk is a member.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsdisk-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the property details of a disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsdisk-queryextents">QueryExtents</a>
</td>
<td align="left" width="63%">
Returns all extents on a disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsdisk-setflags">SetFlags</a>
</td>
<td align="left" width="63%">
Sets the flags of a disk.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/disk-object">Disk Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdspack-querydisks">IVdsPack::QueryDisks</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-vds_disk_prop">VDS_DISK_PROP</a>
 

 

