---
UID: NN:vds.IVdsAdvancedDisk2
title: IVdsAdvancedDisk2 (vds.h)
description: Provides a method to change partition types.
old-location: base\ivdsadvanceddisk2.htm
tech.root: VDS
ms.assetid: 3a6e7bac-3e94-48bd-8aeb-34278a34b0a1
ms.date: 12/05/2018
ms.keywords: IVdsAdvancedDisk2, IVdsAdvancedDisk2 interface, IVdsAdvancedDisk2 interface,described, base.ivdsadvanceddisk2, vds/IVdsAdvancedDisk2
ms.topic: interface
f1_keywords:
- vds/IVdsAdvancedDisk2
dev_langs:
- c++
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- IVdsAdvancedDisk2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsAdvancedDisk2 interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides a method to change partition types.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsAdvancedDisk2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsAdvancedDisk2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsAdvancedDisk2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk2-changepartitiontype">ChangePartitionType</a>
</td>
<td align="left" width="63%">
Changes the partition type on the disk at a specified byte offset.

</td>
</tr>
</table> 

