---
UID: NN:vds.IVdsRemovable
title: IVdsRemovable (vds.h)
description: Provides methods to query and eject a removable disk, such as a CD-ROM.
helpviewer_keywords: ["IVdsRemovable","IVdsRemovable interface [VDS]","IVdsRemovable interface [VDS]","described","base.ivdsremovable","vds/IVdsRemovable"]
old-location: base\ivdsremovable.htm
tech.root: base
ms.assetid: 86dcd76a-0de0-42f4-9360-87cf7ca4ebf6
ms.date: 12/05/2018
ms.keywords: IVdsRemovable, IVdsRemovable interface [VDS], IVdsRemovable interface [VDS],described, base.ivdsremovable, vds/IVdsRemovable
f1_keywords:
- vds/IVdsRemovable
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
- IVdsRemovable
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsRemovable interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods to query and eject a removable disk, such as a CD-ROM.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsRemovable</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsRemovable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsRemovable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsremovable-eject">Eject</a>
</td>
<td align="left" width="63%">
Ejects the media from the current device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsremovable-querymedia">QueryMedia</a>
</td>
<td align="left" width="63%">
Returns the details of the media in a removable disk or CD-ROM/DVD drive.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/disk-object">Disk Object</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

