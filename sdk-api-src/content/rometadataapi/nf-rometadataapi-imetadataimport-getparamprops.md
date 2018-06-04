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

# IMetaDataImport::GetParamProps


## -description


Gets metadata values for the parameter referenced by the specified ParamDef token.


## -parameters




### -param tkParamDef [in]

A ParamDef token that represents the parameter to return metadata for.


### -param ptkMethodDef [out]

A pointer to a MethodDef token representing the method that takes the parameter.


### -param pulSequence [out]

The ordinal position of the parameter in the method argument list.


### -param szName [out]

A buffer to hold the name of the parameter.


### -param cchName [in]

The requested size in wide characters of <i>szName</i>.


### -param pchName [out]

The returned size in wide characters of <i>szName</i>.


### -param pdwAttr [out]

A pointer to any attribute flags associated with the parameter.


### -param pdwCPlusTypeFlag [out]

A pointer to a flag specifying that the parameter is a ValueType.


### -param ppValue [out]

A pointer to a constant string returned by the parameter.


### -param pcchValue [out]

The size of <i>ppValue</i> in wide characters, or zero if <i>ppValue</i> does not hold a string.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

