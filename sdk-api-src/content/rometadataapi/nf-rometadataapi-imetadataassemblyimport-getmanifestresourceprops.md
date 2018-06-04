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

# IMetaDataAssemblyImport::GetManifestResourceProps


## -description


Gets the set of properties of the manifest resource with the specified metadata signature.


## -parameters




### -param mdmr [in]

An <b>mdManifestResource</b> token that represents the resource for which to get the properties.


### -param szName [out]

The name of the resource.


### -param cchName [in]

The size, in wide chars, of <i>szName</i>.


### -param pchName [out]

A pointer to the number of wide chars actually returned in <i>szName</i>.


### -param ptkImplementation [out]

A pointer to an <b>mdFile</b> token or an <b>mdAssemblyRef</b> token that represents the file or assembly, respectively, that contains the resource.


### -param pdwOffset [out]

A pointer to a value that specifies the offset to the beginning of the resource within the file.


### -param pdwResourceFlags [out]

A pointer to flags that describe the metadata applied to a resource. The flags value is a combination of one or more <a href="http://msdn.microsoft.com/en-us/library/ms230274.aspx">CorManifestResourceFlags</a> values.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c4ae6028-87ac-4bb9-8eda-c6a48e5ecd3c">IMetaDataAssemblyImport</a>
 

 

