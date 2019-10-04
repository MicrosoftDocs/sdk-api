---
UID: NN:vdshwprv.IVdsDrive
title: IVdsDrive (vdshwprv.h)
author: windows-sdk-content
description: Provides methods for performing query and configuration operations on a drive.
old-location: base\ivdsdrive.htm
tech.root: VDS
ms.assetid: 597917cf-fb02-4949-98c3-3da3f7449ed1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsDrive, IVdsDrive interface [VDS], IVdsDrive interface [VDS],described, base.ivdsdrive, vds/IVdsDrive, vdshwprv/IVdsDrive
ms.topic: interface
f1_keywords:
- vdshwprv/IVdsDrive
dev_langs:
 - c++
req.header: vdshwprv.h
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
- IVdsDrive
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsDrive interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods for performing query and configuration operations on a drive.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsDrive</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsDrive</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsDrive</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsdrive-clearflags">ClearFlags</a>
</td>
<td align="left" width="63%">
Clears all flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsdrive-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of the drive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsdrive-getsubsystem">GetSubSystem</a>
</td>
<td align="left" width="63%">
Returns the subsystem to which the drive belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsdrive-queryextents">QueryExtents</a>
</td>
<td align="left" width="63%">
Returns an array of extents on a drive, including both allocated and unallocated extents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsdrive-setflags">SetFlags</a>
</td>
<td align="left" width="63%">
Sets flags on a drive object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsdrive-setstatus">SetStatus</a>
</td>
<td align="left" width="63%">
Sets the status of the drive to the specified value.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/drive-object">Drive Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-queryextents">IVdsLunPlex::QueryExtents</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-getdrive">IVdsSubSystem::GetDrive</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-querydrives">IVdsSubSystem::QueryDrives</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_drive_prop">VDS_DRIVE_PROP</a>
 

 

