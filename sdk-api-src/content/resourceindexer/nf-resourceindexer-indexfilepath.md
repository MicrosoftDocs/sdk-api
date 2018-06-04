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

# IndexFilePath function


## -description


Indexes a file path for file and folder naming conventions.


## -parameters




### -param resourceIndexer [in]

The resource indexer object that you created by calling the <a href="https://msdn.microsoft.com/240C94B6-DF61-4C84-9047-9CD81A6FF4B4">CreateResourceIndexer</a> function.


### -param filePath [in]

The path for the folder that you want to index. The path must be an absolute path with the drive letter specified. Long file paths are not supported.


### -param ppResourceUri [out]

A uniform resource indicator (URI) that uses the ms-resource URI scheme and represents the named resource for the candidate, where the authority of the URI or the resource map is empty. For example, ms-resource:///Resources/String1 or ms-resource:///Files/images/logo.png.


### -param pQualifierCount [out]

The number of indexed resource qualifiers that the list in the <i>ppQualifiers</i> parameter contains.


### -param ppQualifiers [out]

A list of indexed resource qualifiers that declare the context under which the resources are appropriate.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/240C94B6-DF61-4C84-9047-9CD81A6FF4B4">CreateResourceIndexer</a>



<a href="https://msdn.microsoft.com/A6F253AD-0756-4996-AC6C-5B09C55DE22E">IndexedResourceQualifier</a>
 

 

