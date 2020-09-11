---
UID: NN:vds.IEnumVdsObject
title: IEnumVdsObject (vds.h)
description: Enumerates through a set of VDS objects of a given type. Objects can be providers, subsystems, controllers, LUNs, LUN plexes, drives, disk packs, disks, volumes, or volume plexes.
helpviewer_keywords: ["IEnumVdsObject","IEnumVdsObject interface [VDS]","IEnumVdsObject interface [VDS]","described","base.ienumvdsobject","vds/IEnumVdsObject","vdshwprv/IEnumVdsObject"]
old-location: base\ienumvdsobject.htm
tech.root: base
ms.assetid: 08379071-b3cc-495a-bc8e-ad6cfacd432c
ms.date: 12/05/2018
ms.keywords: IEnumVdsObject, IEnumVdsObject interface [VDS], IEnumVdsObject interface [VDS],described, base.ienumvdsobject, vds/IEnumVdsObject, vdshwprv/IEnumVdsObject
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumVdsObject
 - vds/IEnumVdsObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IEnumVdsObject
---

# IEnumVdsObject interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Enumerates through a 
   set of VDS objects of a given type. Objects can be providers, subsystems, controllers, LUNs, LUN plexes, drives, 
   disk packs, disks, volumes, or volume plexes.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumVdsObject</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumVdsObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumVdsObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ienumvdsobject-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates an enumeration with the same state as the current enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ienumvdsobject-next">Next</a>
</td>
<td align="left" width="63%">
Returns the next object in the enumeration, beginning from the current point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ienumvdsobject-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ienumvdsobject-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of objects in the enumeration.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/VDS/helper-objects">Helper Objects</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/working-with-enumeration-objects">Working with Enumeration Objects</a>

