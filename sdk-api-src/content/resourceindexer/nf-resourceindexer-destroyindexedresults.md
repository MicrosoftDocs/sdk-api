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

# DestroyIndexedResults function


## -description


Frees the parameters that the <a href="https://msdn.microsoft.com/A1CDA9D1-9FEE-4FCB-AA85-1DA58D9EF95B">IndexFilePath</a> method returned.


## -parameters




### -param resourceUri [in, optional]

A uniform resource indicator (URI) that uses the ms-resource URI scheme and represents the named resource for the candidate, where the authority of the URI or the resource map is empty. For example, ms-resource:///Resources/String1 or ms-resource:///Files/images/logo.png.


### -param qualifierCount [in]

The number of indexed resource qualifiers that the list in the <i>ppQualifiers</i> parameter contains.


### -param qualifiers [in, optional]

A list of indexed resource qualifiers that declare the context under which the resources are appropriate.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/A1CDA9D1-9FEE-4FCB-AA85-1DA58D9EF95B">IndexFilePath</a>



<a href="https://msdn.microsoft.com/A6F253AD-0756-4996-AC6C-5B09C55DE22E">IndexedResourceQualifier</a>
 

 

