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

# IFindSimilarResults::GetSize


## -description


Retrieves the number of entries in the  file list that was returned by the <a href="https://msdn.microsoft.com/70a205fc-d90a-43fc-88f4-2f3a573c5a82">ISimilarity::FindSimilarFileId</a> method.

The actual number of similarity file IDs that are returned by the <a href="https://msdn.microsoft.com/881e0ae6-311f-4bc4-9660-b0e96b7b9bd2">GetNextFileId</a> method may be less than the number that is  returned by the <b>GetSize</b>  method.  <b>GetNextFileId</b> returns only valid similarity file IDs. However, <b>GetSize</b> counts all entries, even if their similarity file IDs are not valid.


## -parameters




### -param size [out]

A pointer to a variable that receives the number of entries in the file list.


## -returns



This method always returns <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/3118cf53-c544-48bc-ac38-79ca2252f83f">IFindSimilarResults</a>
 

 

