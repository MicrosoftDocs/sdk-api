---
UID: NF:rometadataapi.IMetaDataAssemblyImport.EnumAssemblyRefs
title: IMetaDataAssemblyImport::EnumAssemblyRefs (rometadataapi.h)
description: Enumerates the mdAssemblyRef instances that are defined in the assembly manifest.
helpviewer_keywords: ["EnumAssemblyRefs","EnumAssemblyRefs method [Windows Runtime]","EnumAssemblyRefs method [Windows Runtime]","IMetaDataAssemblyImport interface","IMetaDataAssemblyImport interface [Windows Runtime]","EnumAssemblyRefs method","IMetaDataAssemblyImport.EnumAssemblyRefs","IMetaDataAssemblyImport::EnumAssemblyRefs","rometadataapi/IMetaDataAssemblyImport::EnumAssemblyRefs","winrt.imetadataassemblyimport_enumassemblyrefs"]
old-location: winrt\imetadataassemblyimport_enumassemblyrefs.htm
tech.root: WinRT
ms.assetid: 2b5768ef-47fc-4052-bb68-e279a027c887
ms.date: 12/05/2018
ms.keywords: EnumAssemblyRefs, EnumAssemblyRefs method [Windows Runtime], EnumAssemblyRefs method [Windows Runtime],IMetaDataAssemblyImport interface, IMetaDataAssemblyImport interface [Windows Runtime],EnumAssemblyRefs method, IMetaDataAssemblyImport.EnumAssemblyRefs, IMetaDataAssemblyImport::EnumAssemblyRefs, rometadataapi/IMetaDataAssemblyImport::EnumAssemblyRefs, winrt.imetadataassemblyimport_enumassemblyrefs
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
 - IMetaDataAssemblyImport::EnumAssemblyRefs
 - rometadataapi/IMetaDataAssemblyImport::EnumAssemblyRefs
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
 - IMetaDataAssemblyImport.EnumAssemblyRefs
---

# IMetaDataAssemblyImport::EnumAssemblyRefs


## -description

Enumerates the mdAssemblyRef instances that are defined in the assembly manifest.

## -parameters

### -param phEnum [in, out]

A pointer to the enumerator. This must be a null value when the <b>EnumAssemblyRefs</b> method is called for the first time.

### -param rAssemblyRefs [out]

The enumeration of <b>mdAssemblyRef</b> metadata tokens.

### -param cMax [in]

The maximum number of tokens that can be placed in the rAssemblyRefs array.

### -param pcTokens [out]

The number of tokens actually placed in <i>rAssemblyRefs</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumAssemblyRefs</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTokens</i> is set to zero.
 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataassemblyimport">IMetaDataAssemblyImport</a>