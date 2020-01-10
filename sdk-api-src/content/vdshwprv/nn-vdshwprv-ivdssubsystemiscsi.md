---
UID: NN:vdshwprv.IVdsSubSystemIscsi
title: IVdsSubSystemIscsi (vdshwprv.h)
description: Provides methods to query and configure iSCSI targets and portals on a subsystem.
old-location: base\ivdssubsystemiscsi.htm
tech.root: VDS
ms.assetid: e92417b7-6664-4fd7-900f-aedc83291dea
ms.date: 12/05/2018
ms.keywords: IVdsSubSystemIscsi, IVdsSubSystemIscsi interface [VDS], IVdsSubSystemIscsi interface [VDS],described, base.ivdssubsystemiscsi, vds/IVdsSubSystemIscsi, vdshwprv/IVdsSubSystemIscsi
f1_keywords:
- vdshwprv/IVdsSubSystemIscsi
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Uuid.lib
- Uuid.dll
api_name:
- IVdsSubSystemIscsi
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
---

# IVdsSubSystemIscsi interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods to query and configure iSCSI targets and portals on a subsystem.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsSubSystemIscsi</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsSubSystemIscsi</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsSubSystemIscsi</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystemiscsi-createtarget">CreateTarget</a>
</td>
<td align="left" width="63%">
Creates an iSCSI target.</p> (Inherited from <b>IVdsSubSystemIscsi</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystemiscsi-queryportals">QueryPortals</a>
</td>
<td align="left" width="63%">
Returns an object that enumerates the iSCSI portals of the subsystem.</p> (Inherited from <b>IVdsSubSystemIscsi</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystemiscsi-querytargets">QueryTargets</a>
</td>
<td align="left" width="63%">
Returns an object that enumerates the iSCSI targets of the subsystem.</p> (Inherited from <b>IVdsSubSystemIscsi</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystemiscsi-setipsecgrouppresharedkey">SetIpsecGroupPresharedKey</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.</p> (Inherited from <b>IVdsSubSystemIscsi</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

