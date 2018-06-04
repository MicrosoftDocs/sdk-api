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

# IMetaDataAssemblyImport::GetExportedTypeProps


## -description


Gets the set of properties of the exported type with the specified metadata signature.


## -parameters




### -param mdct [in]

An <b>mdExportedType</b> metadata token that represents the exported type.


### -param szName [out]

The name of the exported type.


### -param cchName [in]

The size, in wide characters, of <i>szName</i>.


### -param pchName [out]

The number of wide characters actually returned in <i>szName</i>.


### -param ptkImplementation [out]

 An <b>mdFile</b>, <b>mdAssemblyRef</b>, or <b>mdExportedType</b> metadata token that contains or allows access to the properties of the exported type.


### -param ptkTypeDef [out]

A pointer to an <b>mdTypeDef</b> token that represents a type in the file.


### -param pdwExportedTypeFlags [out]

A pointer to the flags that describe the metadata applied to the exported type. The flags value can be one or more <a href="http://msdn.microsoft.com/en-us/library/ms231889.aspx">CorTypeAttr</a> values.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c4ae6028-87ac-4bb9-8eda-c6a48e5ecd3c">IMetaDataAssemblyImport</a>
 

 

