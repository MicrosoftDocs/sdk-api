---
UID: NN:vds.IVdsIscsiPortalGroup
title: IVdsIscsiPortalGroup (vds.h)
description: Provides methods for performing query and configuration services on an iSCSI portal group.
helpviewer_keywords: ["IVdsIscsiPortalGroup","IVdsIscsiPortalGroup interface [VDS]","IVdsIscsiPortalGroup interface [VDS]","described","base.ivdsiscsiportalgroup","vds/IVdsIscsiPortalGroup","vdshwprv/IVdsIscsiPortalGroup"]
old-location: base\ivdsiscsiportalgroup.htm
tech.root: base
ms.assetid: 65d773bd-3828-4c9d-a841-bb85a53aeadc
ms.date: 12/05/2018
ms.keywords: IVdsIscsiPortalGroup, IVdsIscsiPortalGroup interface [VDS], IVdsIscsiPortalGroup interface [VDS],described, base.ivdsiscsiportalgroup, vds/IVdsIscsiPortalGroup, vdshwprv/IVdsIscsiPortalGroup
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
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - IVdsIscsiPortalGroup
 - vds/IVdsIscsiPortalGroup
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
 - IVdsIscsiPortalGroup
---

# IVdsIscsiPortalGroup interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods for performing query and configuration services on an iSCSI portal group.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsIscsiPortalGroup</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsIscsiPortalGroup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsIscsiPortalGroup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportalgroup-addportal">AddPortal</a>
</td>
<td align="left" width="63%">
Adds a portal to a portal group..</p> (Inherited from <b>IVdsIscsiPortalGroup</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportalgroup-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes the portal group.</p> (Inherited from <b>IVdsIscsiPortalGroup</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportalgroup-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of a portal group.</p> (Inherited from <b>IVdsIscsiPortalGroup</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportalgroup-gettarget">GetTarget</a>
</td>
<td align="left" width="63%">
Returns the target to which the portal group belongs.</p> (Inherited from <b>IVdsIscsiPortalGroup</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportalgroup-queryassociatedportals">QueryAssociatedPortals</a>
</td>
<td align="left" width="63%">
Returns an enumeration of the portals with which the portal group is associated.</p> (Inherited from <b>IVdsIscsiPortalGroup</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportalgroup-removeportal">RemovePortal</a>
</td>
<td align="left" width="63%">
Removes a portal from a portal group.</p> (Inherited from <b>IVdsIscsiPortalGroup</b>)</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>