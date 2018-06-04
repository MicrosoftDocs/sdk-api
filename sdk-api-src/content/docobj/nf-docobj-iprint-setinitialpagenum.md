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

# IPrint::SetInitialPageNum


## -description


Sets the page number of the first page of a document.


## -parameters




### -param nFirstPage [in]

The page number of the first page.


## -returns



This method can return the standard return values E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



Setting the first page to a negative number is valid. This may be useful in printing a portion of the document with page numbers that specify an offset from the usual pagination.

Not all implementations permit the initial page number to be set, as some implementations simply lack the information as to how the page number should be presented in the final output.




## -see-also




<a href="https://msdn.microsoft.com/eb0d15c0-8a34-4211-b840-29d5862cf767">IPrint</a>
 

 

