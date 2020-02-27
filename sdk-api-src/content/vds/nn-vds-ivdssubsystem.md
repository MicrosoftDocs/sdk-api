---
UID: NN:vds.IVdsSubSystem
title: IVdsSubSystem (vds.h)
description: Provides methods for performing query and configuration operations on a subsystem.
old-location: base\ivdssubsystem.htm
tech.root: VDS
ms.assetid: 1f1b9735-216b-4bc5-a9b8-2d274827b2c8
ms.date: 12/05/2018
ms.keywords: IVdsSubSystem, IVdsSubSystem interface [VDS], IVdsSubSystem interface [VDS],described, base.ivdssubsystem, vds/IVdsSubSystem, vdshwprv/IVdsSubSystem
f1_keywords:
- vds/IVdsSubSystem
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
- IVdsSubSystem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsSubSystem interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods for performing query and configuration operations on a subsystem.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsSubSystem</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsSubSystem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsSubSystem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-createlun">CreateLun</a>
</td>
<td align="left" width="63%">
Creates a new LUN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-getdrive">GetDrive</a>
</td>
<td align="left" width="63%">
Returns the specified drive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of the subsystem object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-getprovider">GetProvider</a>
</td>
<td align="left" width="63%">
Returns the provider that manages the subsystem.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-querycontrollers">QueryControllers</a>
</td>
<td align="left" width="63%">
Returns an enumeration of the controllers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-querydrives">QueryDrives</a>
</td>
<td align="left" width="63%">
Returns an enumeration of the drives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-queryluns">QueryLuns</a>
</td>
<td align="left" width="63%">
Returns an enumeration of LUNs surfaced by the subsystem.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-querymaxluncreatesize">QueryMaxLunCreateSize</a>
</td>
<td align="left" width="63%">
Returns the size of the maximum  LUN that can be created using the specified 
    LUN type and hints.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-reenumerate">Reenumerate</a>
</td>
<td align="left" width="63%">
Prompts the subsystem to scan its bus to discover newly connected drives or newly disconnected drives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-replacedrive">ReplaceDrive</a>
</td>
<td align="left" width="63%">
Replaces or migrates one of the drives with another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-setcontrollerstatus">SetControllerStatus</a>
</td>
<td align="left" width="63%">
Sets the controllers to either online or offline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-setstatus">SetStatus</a>
</td>
<td align="left" width="63%">
Sets the status of the subsystem to the specified value.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-getsubsystem">IVdsController::GetSubSystem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsdrive-getsubsystem">IVdsDrive::GetSubSystem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-querysubsystems">IVdsHwProvider::QuerySubSystems</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-getsubsystem">IVdsLun::GetSubSystem</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/subsystem-object">Subsystem Object</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

