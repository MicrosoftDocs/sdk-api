---
UID: NF:rometadataapi.IMetaDataImport.GetFieldProps
title: IMetaDataImport::GetFieldProps method
author: windows-driver-content
description: Gets metadata associated with the field referenced by the specified FieldDef token.
old-location: winrt\imetadataimport_getfieldprops.htm
old-project: WinRT
ms.assetid: 6c935c4c-a7ac-49b9-af26-25f240ef78f2
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: GetFieldProps method [Windows Runtime], GetFieldProps method [Windows Runtime], IMetaDataImport interface, GetFieldProps,IMetaDataImport.GetFieldProps, IMetaDataImport, IMetaDataImport interface [Windows Runtime], GetFieldProps method, IMetaDataImport::GetFieldProps, rometadataapi/IMetaDataImport::GetFieldProps, winrt.imetadataimport_getfieldprops
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	rometadataapi.h
api_name:
-	IMetaDataImport.GetFieldProps
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMetaDataImport::GetFieldProps method


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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

