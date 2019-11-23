---
UID: NN:vdshwprv.IVdsAdmin
title: IVdsAdmin (vdshwprv.h)

description: Registers providers with VDS.
old-location: base\ivdsadmin.htm
tech.root: VDS
ms.assetid: 693ee0c0-9f86-4f78-9724-f3a3420463c9

ms.date: 12/05/2018
ms.keywords: IVdsAdmin, IVdsAdmin interface [VDS], IVdsAdmin interface [VDS],described, base.ivdsadmin, vdshwprv/IVdsAdmin
ms.topic: interface
f1_keywords: 
 - "vdshwprv/IVdsAdmin"
dev_langs:
 - c++
req.header: vdshwprv.h
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
 - IVdsAdmin
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsAdmin interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Registers providers with VDS.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsAdmin</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsAdmin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsAdmin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsadmin-registerprovider">RegisterProvider</a>
</td>
<td align="left" width="63%">
Registers the specified provider with VDS.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsadmin-unregisterprovider">UnregisterProvider</a>
</td>
<td align="left" width="63%">
Deletes VDS provider registration data.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

