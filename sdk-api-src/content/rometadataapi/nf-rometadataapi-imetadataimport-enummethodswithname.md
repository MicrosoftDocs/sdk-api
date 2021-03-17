---
UID: NF:rometadataapi.IMetaDataImport.EnumMethodsWithName
title: IMetaDataImport::EnumMethodsWithName (rometadataapi.h)
description: Enumerates methods that have the specified name and that are defined by the type referenced by the specified TypeDef token.
helpviewer_keywords: ["EnumMethodsWithName","EnumMethodsWithName method [Windows Runtime]","EnumMethodsWithName method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","EnumMethodsWithName method","IMetaDataImport.EnumMethodsWithName","IMetaDataImport::EnumMethodsWithName","rometadataapi/IMetaDataImport::EnumMethodsWithName","winrt.imetadataimport_enummethodswithname"]
old-location: winrt\imetadataimport_enummethodswithname.htm
tech.root: WinRT
ms.assetid: 5252b535-23e5-4af1-91df-006717c4e159
ms.date: 12/05/2018
ms.keywords: EnumMethodsWithName, EnumMethodsWithName method [Windows Runtime], EnumMethodsWithName method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumMethodsWithName method, IMetaDataImport.EnumMethodsWithName, IMetaDataImport::EnumMethodsWithName, rometadataapi/IMetaDataImport::EnumMethodsWithName, winrt.imetadataimport_enummethodswithname
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
 - IMetaDataImport::EnumMethodsWithName
 - rometadataapi/IMetaDataImport::EnumMethodsWithName
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
 - IMetaDataImport.EnumMethodsWithName
---

# IMetaDataImport::EnumMethodsWithName


## -description

Enumerates methods that have the specified name and that are defined by the type referenced by the specified TypeDef token.

## -parameters

### -param phEnum [in, out]

A pointer to the enumerator. This must be NULL for the first call of this method.

### -param tkTypeDef [in]

A TypeDef token representing the type whose methods to enumerate.

### -param szName [in]

The name that limits the scope of the enumeration.

### -param rgMethods [out]

The array used to store the MethodDef tokens.

### -param cMax [in]

The maximum size of the <i>rgMethods</i> array.

### -param pcTokens [out]

The number of MethodDef tokens returned in <i>rgMethods</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumMethodsWithName</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTokens</i> is 0 (zero).
 

</td>
</tr>
</table>

## -remarks

This method enumerates fields and methods, but not properties or events. Unlike <a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataimport-enummethods">EnumMethods</a>, <b>EnumMethodsWithName</b> discards all method tokens that do not have the specified name.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>