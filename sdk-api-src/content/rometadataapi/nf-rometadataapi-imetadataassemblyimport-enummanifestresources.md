---
UID: NF:rometadataapi.IMetaDataAssemblyImport.EnumManifestResources
title: IMetaDataAssemblyImport::EnumManifestResources (rometadataapi.h)
description: Gets a pointer to an enumerator for the resources referenced in the current assembly manifest.
helpviewer_keywords: ["EnumManifestResources","EnumManifestResources method [Windows Runtime]","EnumManifestResources method [Windows Runtime]","IMetaDataAssemblyImport interface","IMetaDataAssemblyImport interface [Windows Runtime]","EnumManifestResources method","IMetaDataAssemblyImport.EnumManifestResources","IMetaDataAssemblyImport::EnumManifestResources","rometadataapi/IMetaDataAssemblyImport::EnumManifestResources","winrt.imetadataassemblyimport_enummanifestresources"]
old-location: winrt\imetadataassemblyimport_enummanifestresources.htm
tech.root: WinRT
ms.assetid: 294ba92f-b6ef-4a66-81b5-b9ff508e147e
ms.date: 12/05/2018
ms.keywords: EnumManifestResources, EnumManifestResources method [Windows Runtime], EnumManifestResources method [Windows Runtime],IMetaDataAssemblyImport interface, IMetaDataAssemblyImport interface [Windows Runtime],EnumManifestResources method, IMetaDataAssemblyImport.EnumManifestResources, IMetaDataAssemblyImport::EnumManifestResources, rometadataapi/IMetaDataAssemblyImport::EnumManifestResources, winrt.imetadataassemblyimport_enummanifestresources
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
 - IMetaDataAssemblyImport::EnumManifestResources
 - rometadataapi/IMetaDataAssemblyImport::EnumManifestResources
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
 - IMetaDataAssemblyImport.EnumManifestResources
---

# IMetaDataAssemblyImport::EnumManifestResources


## -description

Gets a pointer to an enumerator for the resources referenced in the current assembly manifest.

## -parameters

### -param phEnum [in, out]

A pointer to the enumerator. This must be a null value when the <b>EnumManifestResources</b> method is called for the first time.

### -param rManifestResources [out]

The array used to store the <b>mdManifestResource</b> metadata tokens.

### -param cMax [in]

The maximum number of <b>mdManifestResource</b> tokens that can be placed in <i>rManifestResources</i>.

### -param pcTokens [out]

The number of <b>mdManifestResource</b> tokens actually placed in <i>rManifestResources</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumManifestResources</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTokens</i> is set to zero.
 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataassemblyimport">IMetaDataAssemblyImport</a>