---
UID: NN:rometadataapi.IMetaDataDispenserEx
title: IMetaDataDispenserEx (rometadataapi.h)
description: Extends the IMetaDataDispenser interface to provide the capability to control how the metadata APIs operate on the current metadata scope.
helpviewer_keywords: ["IMetaDataDispenserEx","IMetaDataDispenserEx interface [Windows Runtime]","IMetaDataDispenserEx interface [Windows Runtime]","described","rometadataapi/IMetaDataDispenserEx","winrt.imetadatadispenserex"]
old-location: winrt\imetadatadispenserex.htm
tech.root: WinRT
ms.assetid: b61c8d05-6d73-4f84-95b2-2a892f3de77c
ms.date: 12/05/2018
ms.keywords: IMetaDataDispenserEx, IMetaDataDispenserEx interface [Windows Runtime], IMetaDataDispenserEx interface [Windows Runtime],described, rometadataapi/IMetaDataDispenserEx, winrt.imetadatadispenserex
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMetaDataDispenserEx
 - rometadataapi/IMetaDataDispenserEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataDispenserEx
---

# IMetaDataDispenserEx interface


## -description

Extends the <a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatadispenser">IMetaDataDispenser</a> interface to provide the capability to control how the metadata APIs operate on the current metadata scope.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMetaDataDispenserEx</b> interface inherits from <b>IMetaDataDispenser</b>. <b>IMetaDataDispenserEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMetaDataDispenserEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatadispenserex-findassembly">FindAssembly</a>
</td>
<td align="left" width="63%">
Gets the name of the assembly.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatadispenserex-findassemblymodule">FindAssemblyModule</a>
</td>
<td align="left" width="63%">
Finds the name of the assembly module.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatadispenserex-getcorsystemdirectory">GetCORSystemDirectory</a>
</td>
<td align="left" width="63%">
Gets the directory that holds the current common language runtime (CLR). This method is supported only for use by out-of-process debuggers. If called from another component, it will return E_NOTIMPL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatadispenserex-getoption">GetOption</a>
</td>
<td align="left" width="63%">
Gets the value of the specified option for the current metadata scope. The option controls how calls to the current metadata scope are handled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatadispenserex-openscopeonitypeinfo">OpenScopeOnITypeInfo</a>
</td>
<td align="left" width="63%">
Opens the specified scope type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatadispenserex-setoption">SetOption</a>
</td>
<td align="left" width="63%">
Sets the specified option to a given value for the current metadata scope. The option controls how calls to the current metadata scope are handled.

</td>
</tr>
</table>