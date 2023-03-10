---
UID: NF:rometadataapi.IMetaDataImport.EnumProperties
title: IMetaDataImport::EnumProperties (rometadataapi.h)
description: Enumerates PropertyDef tokens representing the properties of the type referenced by the specified TypeDef token.
helpviewer_keywords: ["EnumProperties","EnumProperties method [Windows Runtime]","EnumProperties method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","EnumProperties method","IMetaDataImport.EnumProperties","IMetaDataImport::EnumProperties","rometadataapi/IMetaDataImport::EnumProperties","winrt.imetadataimport_enumproperties"]
old-location: winrt\imetadataimport_enumproperties.htm
tech.root: WinRT
ms.assetid: 54b89188-43d3-4997-aef4-48beaae151da
ms.date: 12/05/2018
ms.keywords: EnumProperties, EnumProperties method [Windows Runtime], EnumProperties method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumProperties method, IMetaDataImport.EnumProperties, IMetaDataImport::EnumProperties, rometadataapi/IMetaDataImport::EnumProperties, winrt.imetadataimport_enumproperties
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
 - IMetaDataImport::EnumProperties
 - rometadataapi/IMetaDataImport::EnumProperties
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
 - IMetaDataImport.EnumProperties
---

# IMetaDataImport::EnumProperties


## -description

Enumerates PropertyDef tokens representing the properties of the type referenced by the specified TypeDef token.

## -parameters

### -param phEnum [in, out]

A pointer to the enumerator. This must be NULL for the first call of this method.

### -param tkTypDef [in]

A TypeDef token representing the type with properties to enumerate.

### -param rgProperties [out]

The array used to store the PropertyDef tokens.

### -param cMax [in]

The maximum size of the <i>rgProperties</i> array.

### -param pcProperties [out]

The number of PropertyDef tokens returned in <i>rgProperties</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumProperties</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcProperties</i> is 0 (zero).
 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>