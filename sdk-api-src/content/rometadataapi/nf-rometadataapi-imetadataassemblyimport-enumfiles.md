---
UID: NF:rometadataapi.IMetaDataAssemblyImport.EnumFiles
title: IMetaDataAssemblyImport::EnumFiles (rometadataapi.h)
description: Enumerates the files referenced in the current assembly manifest.
helpviewer_keywords: ["EnumFiles","EnumFiles method [Windows Runtime]","EnumFiles method [Windows Runtime]","IMetaDataAssemblyImport interface","IMetaDataAssemblyImport interface [Windows Runtime]","EnumFiles method","IMetaDataAssemblyImport.EnumFiles","IMetaDataAssemblyImport::EnumFiles","rometadataapi/IMetaDataAssemblyImport::EnumFiles","winrt.imetadataassemblyimport_enumfiles"]
old-location: winrt\imetadataassemblyimport_enumfiles.htm
tech.root: WinRT
ms.assetid: 4039432e-bcf1-4460-8be7-9f02c250ecc6
ms.date: 12/05/2018
ms.keywords: EnumFiles, EnumFiles method [Windows Runtime], EnumFiles method [Windows Runtime],IMetaDataAssemblyImport interface, IMetaDataAssemblyImport interface [Windows Runtime],EnumFiles method, IMetaDataAssemblyImport.EnumFiles, IMetaDataAssemblyImport::EnumFiles, rometadataapi/IMetaDataAssemblyImport::EnumFiles, winrt.imetadataassemblyimport_enumfiles
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
 - IMetaDataAssemblyImport::EnumFiles
 - rometadataapi/IMetaDataAssemblyImport::EnumFiles
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
 - IMetaDataAssemblyImport.EnumFiles
---

# IMetaDataAssemblyImport::EnumFiles


## -description

Enumerates the files referenced in the current assembly manifest.

## -parameters

### -param phEnum [in, out]

A pointer to the enumerator. This must be a null value for the first call of this method.

### -param rFiles [out]

The array used to store the <b>mdFile</b> metadata tokens.

### -param cMax [in]

The maximum number of <b>mdFile</b> tokens that can be placed in <i>rFiles</i>.

### -param pcTokens [out]

The number of <b>mdFile</b> tokens actually placed in <i>rFiles</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumFiles</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTokens</i> is set to zero.
 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataassemblyimport">IMetaDataAssemblyImport</a>