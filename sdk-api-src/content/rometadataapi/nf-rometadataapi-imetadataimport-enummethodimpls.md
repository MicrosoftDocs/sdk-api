---
UID: NF:rometadataapi.IMetaDataImport.EnumMethodImpls
title: IMetaDataImport::EnumMethodImpls (rometadataapi.h)
description: Enumerates MethodBody and MethodDeclaration tokens representing methods of the specified type.
helpviewer_keywords: ["EnumMethodImpls","EnumMethodImpls method [Windows Runtime]","EnumMethodImpls method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","EnumMethodImpls method","IMetaDataImport.EnumMethodImpls","IMetaDataImport::EnumMethodImpls","rometadataapi/IMetaDataImport::EnumMethodImpls","winrt.imetadataimport_enummethodimpls"]
old-location: winrt\imetadataimport_enummethodimpls.htm
tech.root: WinRT
ms.assetid: 48df8d5a-8fd2-4b36-9fb1-6f45551c1d37
ms.date: 12/05/2018
ms.keywords: EnumMethodImpls, EnumMethodImpls method [Windows Runtime], EnumMethodImpls method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumMethodImpls method, IMetaDataImport.EnumMethodImpls, IMetaDataImport::EnumMethodImpls, rometadataapi/IMetaDataImport::EnumMethodImpls, winrt.imetadataimport_enummethodimpls
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
 - IMetaDataImport::EnumMethodImpls
 - rometadataapi/IMetaDataImport::EnumMethodImpls
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
 - IMetaDataImport.EnumMethodImpls
---

# IMetaDataImport::EnumMethodImpls


## -description

Enumerates MethodBody and MethodDeclaration tokens representing methods of the specified type.

## -parameters

### -param phEnum [in, out]

 A pointer to the enumerator. This must be NULL for the first call of this method.

### -param tkTypeDef [in]

A TypeDef token for the type whose method implementations to enumerate.

### -param rMethodBody [out]

The array to store the MethodBody tokens.

### -param rMethodDecl [out]

The array to store the MethodDeclaration tokens.

### -param cMax [in]

The maximum size of the <i>rMethodBody</i> and <i>rMethodDecl</i> arrays.

### -param pcTokens [out]

The actual number of methods returned in <i>rMethodBody</i> and <i>rMethodDecl</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumMethodImpls</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no method tokens to enumerate. In this case, <i>pcTokens</i> is 0 (zero).
 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>