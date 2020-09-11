---
UID: NN:vds.IVdsLunIscsi
title: IVdsLunIscsi (vds.h)
description: Provides methods for performing query and configuration operations on an iSCSI LUN.
helpviewer_keywords: ["IVdsLunIscsi","IVdsLunIscsi interface [VDS]","IVdsLunIscsi interface [VDS]","described","base.ivdsluniscsi","vds/IVdsLunIscsi","vdshwprv/IVdsLunIscsi"]
old-location: base\ivdsluniscsi.htm
tech.root: base
ms.assetid: 5b1e6204-6cc0-4d94-8e54-fa963f83ae39
ms.date: 12/05/2018
ms.keywords: IVdsLunIscsi, IVdsLunIscsi interface [VDS], IVdsLunIscsi interface [VDS],described, base.ivdsluniscsi, vds/IVdsLunIscsi, vdshwprv/IVdsLunIscsi
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - IVdsLunIscsi
 - vds/IVdsLunIscsi
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - IVdsLunIscsi
---

# IVdsLunIscsi interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides 
   methods for performing query and configuration operations on an iSCSI LUN.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsLunIscsi</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsLunIscsi</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsLunIscsi</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsluniscsi-associatetargets">AssociateTargets</a>
</td>
<td align="left" width="63%">
Associates LUNs with subsystem iSCSI targets.</p> (Inherited from <b>IVdsLunIscsi</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsluniscsi-queryassociatedtargets">QueryAssociatedTargets</a>
</td>
<td align="left" width="63%">
Returns an enumeration of currently associated iSCSI targets—the targets 
   through which the LUN is accessible.</p> (Inherited from <b>IVdsLunIscsi</b>)</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>

