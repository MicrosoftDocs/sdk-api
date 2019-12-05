---
UID: NN:vds.IVdsProvider
title: IVdsProvider (vds.h)
description: Returns the properties of a hardware or software provider.
old-location: base\ivdsprovider.htm
tech.root: VDS
ms.assetid: c09aa32f-d859-44b1-8656-973ba1b6a167
ms.date: 12/05/2018
ms.keywords: IVdsProvider, IVdsProvider interface [VDS], IVdsProvider interface [VDS],described, base.ivdsprovider, vds/IVdsProvider, vdshwprv/IVdsProvider
ms.topic: interface
f1_keywords:
- vds/IVdsProvider
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
- IVdsProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsProvider interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the properties of 
   a hardware or software provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsprovider-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of the provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdspack-getprovider">IVdsPack::GetProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-queryproviders">IVdsService::QueryProviders</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-getprovider">IVdsSubSystem::GetProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/provider-object">Provider Object</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_provider_prop">VDS_PROVIDER_PROP</a>
 

 

