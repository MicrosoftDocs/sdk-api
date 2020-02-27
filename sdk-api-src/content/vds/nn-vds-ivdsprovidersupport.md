---
UID: NN:vds.IVdsProviderSupport
title: IVdsProviderSupport (vds.h)
description: Provides a method to indicate what versions of the VDS interfaces are supported by the provider.
old-location: base\ivdsprovidersupport.htm
tech.root: VDS
ms.assetid: 74e17a86-75ec-429b-9efb-80812ca4b431
ms.date: 12/05/2018
ms.keywords: IVdsProviderSupport, IVdsProviderSupport interface, IVdsProviderSupport interface,described, base.ivdsprovidersupport, vds/IVdsProviderSupport, vdshwprv/IVdsProviderSupport
f1_keywords:
- vds/IVdsProviderSupport
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
- IVdsProviderSupport
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
---

# IVdsProviderSupport interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides a method 
    to indicate what versions of the VDS interfaces are supported by the provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsProviderSupport</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsProviderSupport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsProviderSupport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsprovidersupport-getversionsupport">GetVersionSupport</a>
</td>
<td align="left" width="63%">
Returns a bitmask of values enumerated by 
     <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_version_support_flag">VDS_VERSION_SUPPORT_FLAG</a> indicating the 
     versions of the VDS interfaces supported by this provider.</p> (Inherited from <b>IVdsProviderSupport</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

