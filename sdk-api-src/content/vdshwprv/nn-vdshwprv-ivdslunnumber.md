---
UID: NN:vdshwprv.IVdsLunNumber
title: IVdsLunNumber (vdshwprv.h)
description: Provides a method to query the LUN number for a LUN.
old-location: base\ivdslunnumber.htm
tech.root: VDS
ms.assetid: 77bd95f7-005a-474f-97c4-e211432b447d
ms.date: 12/05/2018
ms.keywords: IVdsLunNumber, IVdsLunNumber interface, IVdsLunNumber interface,described, base.ivdslunnumber, vds/IVdsLunNumber, vdshwprv/IVdsLunNumber
ms.topic: interface
f1_keywords:
- vdshwprv/IVdsLunNumber
dev_langs:
- c++
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
- IVdsLunNumber
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsLunNumber interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides a method to query the LUN number for a LUN.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsLunNumber</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsLunNumber</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsLunNumber</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunnumber-getlunnumber">GetLunNumber</a>
</td>
<td align="left" width="63%">
Retrieves the LUN number for a LUN.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

