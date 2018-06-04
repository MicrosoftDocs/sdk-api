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

# IMetaDataAssemblyImport::GetFileProps


## -description


Gets the properties of the file with the specified metadata signature.


## -parameters




### -param mdf [in]

The <b>mdFile</b> metadata token that represents the file for which to get the properties.


### -param szName [out]

The simple name of the file.


### -param cchName [in]

The size, in wide chars, of <i>szName</i>.


### -param pchName [out]

The number of wide chars actually returned in <i>szName</i>.


### -param ppbHashValue [out]

A pointer to the hash value. This is the hash, using the SHA-1 algorithm, of the file.


### -param pcbHashValue [out]

The number of wide chars in the returned hash value.


### -param pdwFileFlags [out]

A pointer to the flags that describe the metadata applied to a file. The flags value is a combination of one or more <a href="http://msdn.microsoft.com/en-us/library/ms232970.aspx">CorFileFlags</a> values.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c4ae6028-87ac-4bb9-8eda-c6a48e5ecd3c">IMetaDataAssemblyImport</a>
 

 

