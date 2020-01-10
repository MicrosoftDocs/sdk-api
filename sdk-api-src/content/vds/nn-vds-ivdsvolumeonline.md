---
UID: NN:vds.IVdsVolumeOnline
title: IVdsVolumeOnline (vds.h)
description: Provides a method to repair single volumes.
old-location: base\ivdsvolumeonline.htm
tech.root: VDS
ms.assetid: f2b7d9aa-e42c-4d6b-92e0-9d9bfbde1a42
ms.date: 12/05/2018
ms.keywords: IVdsVolumeOnline, IVdsVolumeOnline interface, IVdsVolumeOnline interface,described, base.ivdsvolumeonline, vds/IVdsVolumeOnline
f1_keywords:
- vds/IVdsVolumeOnline
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
- IVdsVolumeOnline
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsVolumeOnline interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides a method to repair  single volumes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsVolumeOnline</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsVolumeOnline</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsVolumeOnline</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumeonline-online">Online</a>
</td>
<td align="left" width="63%">
Returns a volume to the healthy state, if possible.

</td>
</tr>
</table> 

