---
UID: NN:vdshwprv.IVdsSubSystemInterconnect
title: IVdsSubSystemInterconnect (vdshwprv.h)
author: windows-sdk-content
description: Provides a method to query the interconnect types that are supported by a subsystem.
old-location: base\ivdssubsysteminterconnect.htm
tech.root: VDS
ms.assetid: d690827a-4608-4d02-a3bb-5cdb5073b0ad
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsSubSystemInterconnect, IVdsSubSystemInterconnect interface, IVdsSubSystemInterconnect interface,described, base.ivdssubsysteminterconnect, vds/IVdsSubSystemInterconnect, vdshwprv/IVdsSubSystemInterconnect
ms.topic: interface
f1_keywords: ["vdshwprv/IVdsSubSystemInterconnect"]
req.header: vdshwprv.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsSubSystemInterconnect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsSubSystemInterconnect interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides a method to query the interconnect types that are supported by a subsystem.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsSubSystemInterconnect</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsSubSystemInterconnect</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsSubSystemInterconnect</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsysteminterconnect-getsupportedinterconnects">GetSupportedInterconnects</a>
</td>
<td align="left" width="63%">
Returns the interconnect types that the subsystem supports.

</td>
</tr>
</table> 

