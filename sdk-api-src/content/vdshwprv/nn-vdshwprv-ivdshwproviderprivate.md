---
UID: NN:vdshwprv.IVdsHwProviderPrivate
title: IVdsHwProviderPrivate (vdshwprv.h)
description: Provides a method that enables VDS to determine whether the hardware provider manages a specified LUN.
helpviewer_keywords: ["IVdsHwProviderPrivate","IVdsHwProviderPrivate interface [VDS]","IVdsHwProviderPrivate interface [VDS]","described","base.ivdshwproviderprivate","vdshwprv/IVdsHwProviderPrivate"]
old-location: base\ivdshwproviderprivate.htm
tech.root: base
ms.assetid: 7e6dbf9e-9060-46bf-be11-9d9d640a3d36
ms.date: 12/05/2018
ms.keywords: IVdsHwProviderPrivate, IVdsHwProviderPrivate interface [VDS], IVdsHwProviderPrivate interface [VDS],described, base.ivdshwproviderprivate, vdshwprv/IVdsHwProviderPrivate
f1_keywords:
- vdshwprv/IVdsHwProviderPrivate
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
- IVdsHwProviderPrivate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsHwProviderPrivate interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides a method that enables VDS to determine whether the hardware provider manages a specified LUN.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsHwProviderPrivate</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsHwProviderPrivate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsHwProviderPrivate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwproviderprivate-queryifcreatedlun">QueryIfCreatedLun</a>
</td>
<td align="left" width="63%">
Enables VDS to determine whether the hardware provider manages the specified LUN.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

