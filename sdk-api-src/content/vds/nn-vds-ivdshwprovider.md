---
UID: NN:vds.IVdsHwProvider
title: IVdsHwProvider (vds.h)
description: Provides methods for performing query, reenumeration, and refresh operations on a hardware provider.
helpviewer_keywords: ["IVdsHwProvider","IVdsHwProvider interface [VDS]","IVdsHwProvider interface [VDS]","described","base.ivdshwprovider","vds/IVdsHwProvider","vdshwprv/IVdsHwProvider"]
old-location: base\ivdshwprovider.htm
tech.root: base
ms.assetid: ff90875d-f437-4236-a13f-d55a83b778b9
ms.date: 12/05/2018
ms.keywords: IVdsHwProvider, IVdsHwProvider interface [VDS], IVdsHwProvider interface [VDS],described, base.ivdshwprovider, vds/IVdsHwProvider, vdshwprv/IVdsHwProvider
f1_keywords:
- vds/IVdsHwProvider
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
- IVdsHwProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsHwProvider interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods for 
   performing query, reenumeration, and refresh operations on a hardware provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsHwProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsHwProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsHwProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-querysubsystems">QuerySubSystems</a>
</td>
<td align="left" width="63%">
Returns an enumeration of the subsystems managed by the provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">Reenumerate</a>
</td>
<td align="left" width="63%">
Discovers newly connected and disconnected subsystems.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the internally-cached data about existing subsystems managed by the provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-queryproviders">IVdsService::QueryProviders</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/provider-object">Provider Object</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

