---
UID: NN:vds.IVdsServiceHba
title: IVdsServiceHba (vds.h)
description: Provides a method to query HBA ports on the local system.helpviewer_keywords: ["IVdsServiceHba","IVdsServiceHba interface [VDS]","IVdsServiceHba interface [VDS]","described","base.ivdsservicehba","vds/IVdsServiceHba"]
old-location: base\ivdsservicehba.htm
tech.root: VDS
ms.assetid: 0f3375fa-fc17-4808-ac29-a772a9c13850
ms.date: 12/05/2018
ms.keywords: IVdsServiceHba, IVdsServiceHba interface [VDS], IVdsServiceHba interface [VDS],described, base.ivdsservicehba, vds/IVdsServiceHba
f1_keywords:
- vds/IVdsServiceHba
dev_langs:
- c++
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
- IVdsServiceHba
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsServiceHba interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides a method to 
   query HBA ports on the local system.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsServiceHba</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsServiceHba</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsServiceHba</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservicehba-queryhbaports">QueryHbaPorts</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> enumeration object containing 
     a list of the HBA ports known to VDS on the local system.</p> (Inherited from <b>IVdsServiceHba</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

