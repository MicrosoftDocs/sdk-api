---
UID: NN:rometadataapi.IMetaDataDispenser
title: IMetaDataDispenser (rometadataapi.h)
description: Provides methods to create a new metadata scope, or open an existing one.helpviewer_keywords: ["IMetaDataDispenser","IMetaDataDispenser interface [Windows Runtime]","IMetaDataDispenser interface [Windows Runtime]","described","rometadataapi/IMetaDataDispenser","winrt.imetadatadispenser"]
old-location: winrt\imetadatadispenser.htm
tech.root: WinRT
ms.assetid: 3454193d-9068-4032-ae9e-b3087509b0b8
ms.date: 12/05/2018
ms.keywords: IMetaDataDispenser, IMetaDataDispenser interface [Windows Runtime], IMetaDataDispenser interface [Windows Runtime],described, rometadataapi/IMetaDataDispenser, winrt.imetadatadispenser
f1_keywords:
- rometadataapi/IMetaDataDispenser
dev_langs:
- c++
req.header: rometadataapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rometadataapi.idl
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
- rometadataapi.h
api_name:
- IMetaDataDispenser
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMetaDataDispenser interface


## -description


Provides methods to create a new metadata scope, or open an existing one.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMetaDataDispenser</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMetaDataDispenser</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMetaDataDispenser</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatadispenser-definescope">DefineScope</a>
</td>
<td align="left" width="63%">
Creates a new area in memory in which you can create new metadata.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatadispenser-openscope">OpenScope</a>
</td>
<td align="left" width="63%">
Opens an existing, on-disk file and maps its metadata into memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatadispenser-openscopeonmemory">OpenScopeOnMemory</a>
</td>
<td align="left" width="63%">
Opens an area of memory that contains existing metadata. 

</td>
</tr>
</table> 

