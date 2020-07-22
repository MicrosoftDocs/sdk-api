---
UID: NN:vsprov.IVssHardwareSnapshotProviderEx
title: IVssHardwareSnapshotProviderEx (vsprov.h)
description: Provides an additional method used by VSS to notify hardware providers of LUN state changes.
helpviewer_keywords: ["IVssHardwareSnapshotProviderEx","IVssHardwareSnapshotProviderEx interface","IVssHardwareSnapshotProviderEx interface","described","base.ivsshardwaresnapshotproviderex","vsprov/IVssHardwareSnapshotProviderEx"]
old-location: base\ivsshardwaresnapshotproviderex.htm
tech.root: base
ms.assetid: aaf94823-845b-49cb-8599-962229fef4cb
ms.date: 12/05/2018
ms.keywords: IVssHardwareSnapshotProviderEx, IVssHardwareSnapshotProviderEx interface, IVssHardwareSnapshotProviderEx interface,described, base.ivsshardwaresnapshotproviderex, vsprov/IVssHardwareSnapshotProviderEx
f1_keywords:
- vsprov/IVssHardwareSnapshotProviderEx
dev_langs:
- c++
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- VsProv.h
api_name:
- IVssHardwareSnapshotProviderEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssHardwareSnapshotProviderEx interface


## -description


Provides an additional method used by VSS to notify hardware providers of LUN state changes. All hardware providers must support this 
   interface.
<div class="alert"><b>Note</b>  Hardware providers are only supported on Windows Server operating systems.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssHardwareSnapshotProviderEx</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nn-vsprov-ivsshardwaresnapshotprovider">IVssHardwareSnapshotProvider</a>. <b>IVssHardwareSnapshotProviderEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssHardwareSnapshotProviderEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotproviderex-getprovidercapabilities">GetProviderCapabilities</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotproviderex-onlunstatechange">OnLunStateChange</a>
</td>
<td align="left" width="63%">
The VSS service calls this method to notify hardware providers of a LUN state change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotproviderex-onreuseluns">OnReuseLuns</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns">ResyncLuns</a>
</td>
<td align="left" width="63%">
The VSS service calls this method to notify hardware providers that a LUN resynchronization is needed.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nn-vsprov-ivsshardwaresnapshotprovider">IVssHardwareSnapshotProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/VSS/volume-shadow-copy-api-interfaces">Volume Shadow Copy API Interfaces</a>
 

 

