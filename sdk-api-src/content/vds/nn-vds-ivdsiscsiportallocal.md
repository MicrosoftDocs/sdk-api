---
UID: NN:vds.IVdsIscsiPortalLocal
title: IVdsIscsiPortalLocal (vds.h)
description: Provides methods for setting local-initiator-specific IPSEC pre-shared keys on an iSCSI portal.
helpviewer_keywords: ["IVdsIscsiPortalLocal","IVdsIscsiPortalLocal interface [VDS]","IVdsIscsiPortalLocal interface [VDS]","described","base.ivdsiscsiportallocal","vds/IVdsIscsiPortalLocal"]
old-location: base\ivdsiscsiportallocal.htm
tech.root: base
ms.assetid: eec436c4-73a6-43c5-aae2-dcdd37eb5767
ms.date: 12/05/2018
ms.keywords: IVdsIscsiPortalLocal, IVdsIscsiPortalLocal interface [VDS], IVdsIscsiPortalLocal interface [VDS],described, base.ivdsiscsiportallocal, vds/IVdsIscsiPortalLocal
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
 - IVdsIscsiPortalLocal
 - vds/IVdsIscsiPortalLocal
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
 - IVdsIscsiPortalLocal
---

# IVdsIscsiPortalLocal interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods for setting local-initiator-specific IPSEC pre-shared keys on an iSCSI portal.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsIscsiPortalLocal</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsIscsiPortalLocal</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsIscsiPortalLocal</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vds/nf-vds-ivdsiscsiportallocal-setipsecsecuritylocal">SetIpsecSecurityLocal</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.</p> (Inherited from <b>IVdsIscsiPortalLocal</b>)</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>