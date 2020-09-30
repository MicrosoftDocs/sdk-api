---
UID: NN:vdshwprv.IVdsProviderPrivate
title: IVdsProviderPrivate (vdshwprv.h)
description: Provides methods to enable VDS to perform miscellaneous operations on provider objects.
helpviewer_keywords: ["IVdsProviderPrivate","IVdsProviderPrivate interface [VDS]","IVdsProviderPrivate interface [VDS]","described","base.ivdsproviderprivate","vdshwprv/IVdsProviderPrivate"]
old-location: base\ivdsproviderprivate.htm
tech.root: base
ms.assetid: 5f1c38bf-85a7-4123-becb-e8abf3052b41
ms.date: 12/05/2018
ms.keywords: IVdsProviderPrivate, IVdsProviderPrivate interface [VDS], IVdsProviderPrivate interface [VDS],described, base.ivdsproviderprivate, vdshwprv/IVdsProviderPrivate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsProviderPrivate
 - vdshwprv/IVdsProviderPrivate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsProviderPrivate
---

# IVdsProviderPrivate interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods to enable VDS to perform miscellaneous operations on provider objects.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsProviderPrivate</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsProviderPrivate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsProviderPrivate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsproviderprivate-getobject">GetObject</a>
</td>
<td align="left" width="63%">
Returns the specified VDS object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsproviderprivate-onload">OnLoad</a>
</td>
<td align="left" width="63%">
Prompts the provider to initialize itself, and passes a callback object that the provider uses to get necessary interfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsproviderprivate-onunload">OnUnload</a>
</td>
<td align="left" width="63%">
Prompts the provider to uninitialize itself.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>