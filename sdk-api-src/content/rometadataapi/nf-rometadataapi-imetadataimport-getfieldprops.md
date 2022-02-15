---
UID: NF:rometadataapi.IMetaDataImport.GetFieldProps
title: IMetaDataImport::GetFieldProps (rometadataapi.h)
description: Gets metadata associated with the field referenced by the specified FieldDef token.
helpviewer_keywords: ["GetFieldProps","GetFieldProps method [Windows Runtime]","GetFieldProps method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","GetFieldProps method","IMetaDataImport.GetFieldProps","IMetaDataImport::GetFieldProps","rometadataapi/IMetaDataImport::GetFieldProps","winrt.imetadataimport_getfieldprops"]
old-location: winrt\imetadataimport_getfieldprops.htm
tech.root: WinRT
ms.assetid: 6c935c4c-a7ac-49b9-af26-25f240ef78f2
ms.date: 12/05/2018
ms.keywords: GetFieldProps, GetFieldProps method [Windows Runtime], GetFieldProps method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetFieldProps method, IMetaDataImport.GetFieldProps, IMetaDataImport::GetFieldProps, rometadataapi/IMetaDataImport::GetFieldProps, winrt.imetadataimport_getfieldprops
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
 - IMetaDataImport::GetFieldProps
 - rometadataapi/IMetaDataImport::GetFieldProps
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
 - IMetaDataImport.GetFieldProps
---

# IMetaDataImport::GetFieldProps


## -description

Gets metadata associated with the field referenced by the specified FieldDef token.

## -parameters

### -param tkFieldDef [in]

A FieldDef token that represents the field to get associated metadata for.

### -param ptkTypeDef [out]

A pointer to a TypeDef token that represents the type of the class that the field belongs to.

### -param szField [out]

The name of the field.

### -param cchField [in]

The size in wide characters of the buffer for <i>szField</i>.

### -param pchField [out]

The actual size of the returned buffer.

### -param pdwAttr [out]

Flags associated with the field's metadata.

### -param ppvSigBlob [out]

A pointer to the binary metadata value that describes the field.

### -param pcbSigBlob [out]

The size in bytes of <i>ppvSigBlob</i>.

### -param pdwCPlusTypeFlag [out]

A flag that specifies the value type of the field.

### -param ppValue [out]

A constant value for the field.

### -param pcchValue [out]

The size in chars of <i>ppValue</i>, or zero if no string exists.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>