---
UID: NF:rometadataapi.IMetaDataImport.EnumTypeDefs
title: IMetaDataImport::EnumTypeDefs (rometadataapi.h)
description: Enumerates TypeDef tokens representing all types within the current scope.
helpviewer_keywords: ["EnumTypeDefs","EnumTypeDefs method [Windows Runtime]","EnumTypeDefs method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","EnumTypeDefs method","IMetaDataImport.EnumTypeDefs","IMetaDataImport::EnumTypeDefs","rometadataapi/IMetaDataImport::EnumTypeDefs","winrt.imetadataimport_enumtypedefs"]
old-location: winrt\imetadataimport_enumtypedefs.htm
tech.root: WinRT
ms.assetid: 64dc7018-721f-4747-b798-fbf70bac18d5
ms.date: 12/05/2018
ms.keywords: EnumTypeDefs, EnumTypeDefs method [Windows Runtime], EnumTypeDefs method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumTypeDefs method, IMetaDataImport.EnumTypeDefs, IMetaDataImport::EnumTypeDefs, rometadataapi/IMetaDataImport::EnumTypeDefs, winrt.imetadataimport_enumtypedefs
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
 - IMetaDataImport::EnumTypeDefs
 - rometadataapi/IMetaDataImport::EnumTypeDefs
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
 - IMetaDataImport.EnumTypeDefs
---

# IMetaDataImport::EnumTypeDefs


## -description

Enumerates TypeDef tokens representing all types within the current scope.

## -parameters

### -param phEnum [in, out]

A pointer to the new enumerator. This must be NULL for the first call of this method.

### -param rgTypeDefs [out]

The array used to store the TypeDef tokens.

### -param cMax [in]

The maximum size of the <i>rgTypeDefs</i> array.

### -param pcTypeDefs [out, retval]

The number of TypeDef tokens returned in <i>rgTypeDefs</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumTypeDefs</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTypeDefs</i> is 0 (zero).
 

</td>
</tr>
</table>

## -remarks

The TypeDef token represents a type such as a class or an interface, as well as any type added via an extensibility mechanism.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>