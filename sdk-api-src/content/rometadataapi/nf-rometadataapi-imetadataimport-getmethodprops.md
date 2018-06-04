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

# IMetaDataImport::GetMethodProps


## -description


Gets the metadata associated with the method referenced by the specified MethodDef token.


## -parameters




### -param tkMethodDef [in]

The MethodDef token that represents the method to return metadata for.


### -param ptkClass [out]

A Pointer to a TypeDef token that represents the type that implements the method.


### -param szMethod [out]

A Pointer to a buffer that has the method's name.


### -param cchMethod [in]

The requested size of <i>szMethod</i>.


### -param pchMethod [out]

A pointer to the size in wide characters of <i>szMethod</i>, or in the case of truncation, the actual number of wide characters in the method name.


### -param pdwAttr [out]

A pointer to any flags associated with the method.


### -param ppvSigBlob [out]

A pointer to the binary metadata signature of the method.


### -param pcbSigBlob [out]

A pointer to the size in bytes of <i>ppvSigBlob</i>.


### -param pulCodeRVA [out]

A pointer to the relative virtual address of the method.


### -param pdwImplFlags [out]

A pointer to any implementation flags for the method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

