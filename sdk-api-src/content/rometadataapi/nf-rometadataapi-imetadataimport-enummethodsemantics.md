---
UID: NF:rometadataapi.IMetaDataImport.EnumMethodSemantics
title: IMetaDataImport::EnumMethodSemantics (rometadataapi.h)
description: Enumerates the properties and the property-change events to which the specified method is related.
helpviewer_keywords: ["EnumMethodSemantics","EnumMethodSemantics method [Windows Runtime]","EnumMethodSemantics method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","EnumMethodSemantics method","IMetaDataImport.EnumMethodSemantics","IMetaDataImport::EnumMethodSemantics","rometadataapi/IMetaDataImport::EnumMethodSemantics","winrt.imetadataimport_enummethodsemantics"]
old-location: winrt\imetadataimport_enummethodsemantics.htm
tech.root: WinRT
ms.assetid: 2b3be5bb-1da7-40d7-8407-c08c2f2723e5
ms.date: 12/05/2018
ms.keywords: EnumMethodSemantics, EnumMethodSemantics method [Windows Runtime], EnumMethodSemantics method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumMethodSemantics method, IMetaDataImport.EnumMethodSemantics, IMetaDataImport::EnumMethodSemantics, rometadataapi/IMetaDataImport::EnumMethodSemantics, winrt.imetadataimport_enummethodsemantics
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
 - IMetaDataImport::EnumMethodSemantics
 - rometadataapi/IMetaDataImport::EnumMethodSemantics
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
 - IMetaDataImport.EnumMethodSemantics
---

# IMetaDataImport::EnumMethodSemantics


## -description

Enumerates the properties and the property-change events to which the specified method is related.

## -parameters

### -param phEnum [in, out]

A pointer to the enumerator. This must be NULL for the first call of this method.

### -param tkMethodDef [in]

 A MethodDef token that limits the scope of the enumeration.

### -param rgEventProp [out]

The array used to store the events or properties.

### -param cMax [in]

The maximum size of the <i>rgEventProp</i> array.

### -param pcEventProp [out]

The number of events or properties returned in <i>rgEventProp</i>.

## -returns

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumMethodSemantics</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no events or properties to enumerate. In this case, <i>pcEventProp</i> is 0 (zero).
 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>