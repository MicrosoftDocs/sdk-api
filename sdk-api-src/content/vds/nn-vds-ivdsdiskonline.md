---
UID: NN:vds.IVdsDiskOnline
title: IVdsDiskOnline (vds.h)
description: Provides methods to bring a disk online and take it offline.Windows Vista:  This interface is not supported until Windows Vista with Service Pack 1 (SP1). Use IVdsDisk2 instead.
helpviewer_keywords: ["IVdsDiskOnline","IVdsDiskOnline interface","IVdsDiskOnline interface","described","base.ivdsdiskonline","vds/IVdsDiskOnline"]
old-location: base\ivdsdiskonline.htm
tech.root: base
ms.assetid: f30ceaa0-ff4b-49fb-b140-b6725810cd06
ms.date: 12/05/2018
ms.keywords: IVdsDiskOnline, IVdsDiskOnline interface, IVdsDiskOnline interface,described, base.ivdsdiskonline, vds/IVdsDiskOnline
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsDiskOnline
 - vds/IVdsDiskOnline
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
 - IVdsDiskOnline
---

# IVdsDiskOnline interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods to bring a disk online and take it offline.<b>Windows Vista:  </b>This interface is not supported until Windows Vista with Service Pack 1 (SP1). Use <a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsdisk2">IVdsDisk2</a> instead.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsDiskOnline</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsDiskOnline</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsDiskOnline</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsdiskonline-offline">Offline</a>
</td>
<td align="left" width="63%">
Takes the disk offline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsdiskonline-online">Online</a>
</td>
<td align="left" width="63%">
Brings the disk online.

</td>
</tr>
</table>

