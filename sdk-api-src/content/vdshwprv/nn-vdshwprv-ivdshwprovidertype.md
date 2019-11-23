---
UID: NN:vdshwprv.IVdsHwProviderType
title: IVdsHwProviderType (vdshwprv.h)

description: Provides a method to retrieve the type of hardware provider.
old-location: base\ivdshwprovidertype.htm
tech.root: VDS
ms.assetid: 24bd634e-96e1-4f2a-a70b-3aae734c75f9

ms.date: 12/05/2018
ms.keywords: IVdsHwProviderType, IVdsHwProviderType interface [VDS], IVdsHwProviderType interface [VDS],described, base.ivdshwprovidertype, vds/IVdsHwProviderType, vdshwprv/IVdsHwProviderType
ms.topic: interface
f1_keywords: 
 - "vdshwprv/IVdsHwProviderType"
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
 - IVdsHwProviderType
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
---

# IVdsHwProviderType interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides a method to retrieve the type of hardware provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsHwProviderType</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsHwProviderType</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsHwProviderType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovidertype-getprovidertype">GetProviderType</a>
</td>
<td align="left" width="63%">
Retrieves the type of the hardware provider.</p> (Inherited from <b>IVdsHwProviderType</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/provider-object">Provider Object</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

