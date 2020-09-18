---
UID: NN:vds.IVdsLun2
title: IVdsLun2 (vds.h)
description: Provides methods for applying and querying logical unit number (LUN) hints.
helpviewer_keywords: ["IVdsLun2","IVdsLun2 interface","IVdsLun2 interface","described","base.ivdslun2","vds/IVdsLun2","vdshwprv/IVdsLun2"]
old-location: base\ivdslun2.htm
tech.root: base
ms.assetid: 1cc26b91-d77b-4f8d-8c01-40b58cb03038
ms.date: 12/05/2018
ms.keywords: IVdsLun2, IVdsLun2 interface, IVdsLun2 interface,described, base.ivdslun2, vds/IVdsLun2, vdshwprv/IVdsLun2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsLun2
 - vds/IVdsLun2
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
 - IVdsLun2
---

# IVdsLun2 interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods for applying and querying logical unit number (LUN) hints.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsLun2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsLun2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsLun2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun2-applyhints2">ApplyHints2</a>
</td>
<td align="left" width="63%">
Applies a new set of 
   hints to the LUN. Hints that are applied to a LUN are simultaneously applied to all plexes. This method is identical to the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-applyhints">IVdsLun::ApplyHints</a> method, except that it uses a <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints2">VDS_HINTS2</a> structure instead of a <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints">VDS_HINTS</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun2-queryhints2">QueryHints2</a>
</td>
<td align="left" width="63%">
Returns the hints 
   currently applied to the LUN. This method is identical to the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-queryhints">IVdsLun::QueryHints</a> method, except that it uses a <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints2">VDS_HINTS2</a> structure instead of a <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints">VDS_HINTS</a> structure.

</td>
</tr>
</table>