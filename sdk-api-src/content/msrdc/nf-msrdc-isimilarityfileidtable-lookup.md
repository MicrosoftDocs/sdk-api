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

# ISimilarityFileIdTable::Lookup


## -description


Retrieves the file ID that corresponds to a given file index in the similarity file ID table.


## -parameters




### -param similarityFileIndex [in]

The file index that was previously returned for the file ID by the <a href="https://msdn.microsoft.com/2157d6e6-0d60-45a2-9f5c-4096088cb2bb">ISimilarityFileIdTable::Append</a> method.


### -param similarityFileId [out]

A pointer to a variable that receives the file ID. If the file has been marked as not valid, the file ID receives zero.


## -returns



Returns <b>S_OK</b> on success, or an error <b>HRESULT</b> on failure.

This method can also return the following error code.




## -see-also




<a href="https://msdn.microsoft.com/539a2e9b-9719-4012-bb7f-4d14723a3695">ISimilarityFileIdTable</a>
 

 

