---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

