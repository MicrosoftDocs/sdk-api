---
UID: NN:vdshwprv.IVdsIscsiPortal
title: IVdsIscsiPortal (vdshwprv.h)
description: Provides methods for performing query and configuration operations on an iSCSI portal.
helpviewer_keywords: ["IVdsIscsiPortal","IVdsIscsiPortal interface [VDS]","IVdsIscsiPortal interface [VDS]","described","base.ivdsiscsiportal","vds/IVdsIscsiPortal","vdshwprv/IVdsIscsiPortal"]
old-location: base\ivdsiscsiportal.htm
tech.root: base
ms.assetid: 1f3131a6-01ab-41e5-9e2f-6ffcdcd0e3a6
ms.date: 12/05/2018
ms.keywords: IVdsIscsiPortal, IVdsIscsiPortal interface [VDS], IVdsIscsiPortal interface [VDS],described, base.ivdsiscsiportal, vds/IVdsIscsiPortal, vdshwprv/IVdsIscsiPortal
req.header: vdshwprv.h
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
 - IVdsIscsiPortal
 - vdshwprv/IVdsIscsiPortal
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
 - IVdsIscsiPortal
---

# IVdsIscsiPortal interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides 
   methods for performing query and configuration operations on an iSCSI portal.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsIscsiPortal</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsIscsiPortal</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsIscsiPortal</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportal-getipsecsecurity">GetIpsecSecurity</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.</p> (Inherited from <b>IVdsIscsiPortal</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportal-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of a portal.</p> (Inherited from <b>IVdsIscsiPortal</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportal-getsubsystem">GetSubSystem</a>
</td>
<td align="left" width="63%">
Returns the subsystem to which the portal belongs.</p> (Inherited from <b>IVdsIscsiPortal</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportal-queryassociatedportalgroups">QueryAssociatedPortalGroups</a>
</td>
<td align="left" width="63%">
Returns an enumeration of the portal groups with which the portal is associated.</p> (Inherited from <b>IVdsIscsiPortal</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportal-setipsecsecurity">SetIpsecSecurity</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.</p> (Inherited from <b>IVdsIscsiPortal</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportal-setipsectunneladdress">SetIpsecTunnelAddress</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.</p> (Inherited from <b>IVdsIscsiPortal</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportal-setstatus">SetStatus</a>
</td>
<td align="left" width="63%">
Sets the status of a portal to the specified value.</p> (Inherited from <b>IVdsIscsiPortal</b>)</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>

