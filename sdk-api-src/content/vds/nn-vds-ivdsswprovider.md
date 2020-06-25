---
UID: NN:vds.IVdsSwProvider
title: IVdsSwProvider (vds.h)
description: Provides methods to perform operations specific to the software provider.
helpviewer_keywords: ["IVdsSwProvider","IVdsSwProvider interface [VDS]","IVdsSwProvider interface [VDS]","described","base.ivdsswprovider","vds/IVdsSwProvider"]
old-location: base\ivdsswprovider.htm
tech.root: VDS
ms.assetid: 0602d4d6-a31d-4425-ad21-a267c6e1dd7b
ms.date: 12/05/2018
ms.keywords: IVdsSwProvider, IVdsSwProvider interface [VDS], IVdsSwProvider interface [VDS],described, base.ivdsswprovider, vds/IVdsSwProvider
f1_keywords:
- vds/IVdsSwProvider
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
- IVdsSwProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsSwProvider interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods to perform operations specific to the software provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsSwProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsSwProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsSwProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsswprovider-createpack">CreatePack</a>
</td>
<td align="left" width="63%">
Creates a disk pack for the current software provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsswprovider-querypacks">QueryPacks</a>
</td>
<td align="left" width="63%">
Returns an enumeration object that contains all packs managed by the software provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/provider-object">Provider Object</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

