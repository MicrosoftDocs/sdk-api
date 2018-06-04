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

# IMetaDataImport::GetTypeDefProps


## -description


Returns metadata information for the Type represented by the specified TypeDef token.


## -parameters




### -param tkTypeDef [in]

The TypeDef token that represents the type to return metadata for.


### -param szTypeDef [out]

A buffer containing the type name.


### -param cchTypeDef [in]

The size in wide characters of <i>szTypeDef</i>.


### -param pchTypeDef [out]

The number of wide characters returned in <i>szTypeDef</i>.


### -param pdwTypeDefFlags [out]

A pointer to any flags that modify the type definition. This value is a bitmask from the <a href="http://msdn.microsoft.com/en-us/library/ms231889.aspx">CorTypeAttr</a> enumeration.


### -param ptkExtends [out]

A TypeDef or TypeRef metadata token that represents the base type of the requested type.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

