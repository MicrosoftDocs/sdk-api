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

# IRoMetaDataLocator structure


## -description


Enables the <a href="https://msdn.microsoft.com/DE908C82-5D7C-415C-B08B-31786589979B">RoGetParameterizedTypeInstanceIID</a> function to access run-time metadata.

Implement <b>IRoMetaDataLocator</b> when you're implementing programming language bindings to enable a language to call Windows platform APIs by using Windows metadata (.winmd) files.




## -struct-fields






#### - Locate

Gets a metadata builder for the specified type.



#### nameElement

A Windows Runtime type or parameterized type to resolve.



#### metaDataDestination

A data sink for Windows Runtime metadata. The caller should invoke the appropriate set method to provide the metadata for the type named by <i>nameElement</i>.


## -see-also




<a href="https://msdn.microsoft.com/FF4FEA9F-3FB0-4D56-BE9A-E8E2CB13D718">RoGetMetaDataFile</a>
 

 

