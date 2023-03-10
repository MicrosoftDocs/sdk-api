---
UID: NF:rometadataapi.IMetaDataImport.EnumCustomAttributes
title: IMetaDataImport::EnumCustomAttributes (rometadataapi.h)
description: Enumerates custom attribute-definition tokens associated with the specified type or member.
helpviewer_keywords: ["EnumCustomAttributes","EnumCustomAttributes method [Windows Runtime]","EnumCustomAttributes method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","EnumCustomAttributes method","IMetaDataImport.EnumCustomAttributes","IMetaDataImport::EnumCustomAttributes","rometadataapi/IMetaDataImport::EnumCustomAttributes","winrt.imetadataimport_enumcustomattributes"]
old-location: winrt\imetadataimport_enumcustomattributes.htm
tech.root: WinRT
ms.assetid: d5ecb71e-a52f-421b-aab9-48efcc77ec2f
ms.date: 12/05/2018
ms.keywords: EnumCustomAttributes, EnumCustomAttributes method [Windows Runtime], EnumCustomAttributes method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumCustomAttributes method, IMetaDataImport.EnumCustomAttributes, IMetaDataImport::EnumCustomAttributes, rometadataapi/IMetaDataImport::EnumCustomAttributes, winrt.imetadataimport_enumcustomattributes
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
 - IMetaDataImport::EnumCustomAttributes
 - rometadataapi/IMetaDataImport::EnumCustomAttributes
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
 - IMetaDataImport.EnumCustomAttributes
---

# IMetaDataImport::EnumCustomAttributes


## -description

Enumerates custom attribute-definition tokens associated with the specified type or member.

## -parameters

### -param phEnum [in, out]

A pointer to the returned enumerator.

### -param tk [in]

 A token for the scope of the enumeration, or zero for all custom attributes.

### -param tkType [in]

A token for the type of the attributes to be enumerated, or zero for all types.

### -param rgCustomAttributes [out]

An array of custom attribute tokens.

### -param cMax [in]

The maximum size of the <i>rgCustomAttributes</i> array.

### -param pcCustomAttributes [out]

The actual number of token values returned in <i>rgCustomAttributes</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumCustomAttributes</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no custom attributes to enumerate. In this case, <i>pcCustomAttributes</i> is 0 (zero).
 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>