---
UID: NN:vdshwprv.IVdsHwProviderPrivateMpio
title: IVdsHwProviderPrivateMpio (vdshwprv.h)
description: Provides a method that sets the status of paths originating from a particular HBA port to the provider.
helpviewer_keywords: ["IVdsHwProviderPrivateMpio","IVdsHwProviderPrivateMpio interface [VDS]","IVdsHwProviderPrivateMpio interface [VDS]","described","base.ivdshwproviderprivatempio","vdshwprv/IVdsHwProviderPrivateMpio"]
old-location: base\ivdshwproviderprivatempio.htm
tech.root: VDS
ms.assetid: fa60e832-1148-4ffb-bf70-bd7b27180cdd
ms.date: 12/05/2018
ms.keywords: IVdsHwProviderPrivateMpio, IVdsHwProviderPrivateMpio interface [VDS], IVdsHwProviderPrivateMpio interface [VDS],described, base.ivdshwproviderprivatempio, vdshwprv/IVdsHwProviderPrivateMpio
f1_keywords:
- vdshwprv/IVdsHwProviderPrivateMpio
dev_langs:
- c++
req.header: vdshwprv.h
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
- IVdsHwProviderPrivateMpio
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsHwProviderPrivateMpio interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides a method that sets the status of paths originating from a particular HBA port to the provider.
  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsHwProviderPrivateMpio</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsHwProviderPrivateMpio</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsHwProviderPrivateMpio</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwproviderprivatempio-setallpathstatusesfromhbaport">SetAllPathStatusesFromHbaPort</a>
</td>
<td align="left" width="63%">
Sets the statuses of paths originating from a particular HBA port to a specified status.</p> (Inherited from <b>IVdsHwProviderPrivateMpio</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdscontroller">IVdsController</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwproviderprivatempio-setallpathstatusesfromhbaport">SetAllPathStatusesFromHbaPort</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

