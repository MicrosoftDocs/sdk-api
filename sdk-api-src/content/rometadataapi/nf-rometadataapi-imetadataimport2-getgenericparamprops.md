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

# IMetaDataImport2::GetGenericParamProps


## -description


Gets the metadata associated with the generic parameter represented by the specified token.


## -parameters




### -param gp [in]

The token that represents the generic parameter for which to return metadata.


### -param pulParamSeq [out]

The ordinal position of the Type parameter in the parent constructor or method.


### -param pdwParamFlags [out]

 A value of the <a href="http://msdn.microsoft.com/en-us/library/ms230535.aspx">CorGenericParamAttr</a> enumeration that describes the Type for the generic parameter.


### -param ptOwner [out]

A  <b>TypeDef</b> or <b>MethodDef</b> token that represents the owner of the parameter.


### -param reserved [out]

Reserved for future extensibility.


### -param wzname [out]

The name of the generic parameter.


### -param cchName [in]

The size of the <i>wzName</i> buffer.


### -param pchName [out]

The returned size of the name, in wide characters.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/32c462e0-d4b8-44db-b24b-c86b46be85bf">IMetaDataImport2</a>
 

 

