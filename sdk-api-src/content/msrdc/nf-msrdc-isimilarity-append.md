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

# ISimilarity::Append


## -description


Adds the file ID and similarity data information to the tables in the similarity file.


## -parameters




### -param similarityFileId [in]

A pointer to the <a href="https://msdn.microsoft.com/07fcb382-726c-4615-83e9-f69eec778311">SimilarityFileId</a> structure to be added to the similarity file ID table.


### -param similarityData [in]

A pointer to the <a href="https://msdn.microsoft.com/33fdb48c-6f33-44e8-83b1-6029b1eace1d">SimilarityData</a> structure to be added to the similarity traits table.


## -returns



Returns <b>S_OK</b> on success, or an error <b>HRESULT</b> on failure.

This method can also return the following error codes.




## -remarks



If this method fails, the similarity file ID table and the similarity traits table are marked as corrupted and must be rebuilt by the application. The application must close the corrupted tables and create new tables.




## -see-also




<a href="https://msdn.microsoft.com/fe0cd874-a40c-4d82-99bf-b84008a4995c">ISimilarity</a>
 

 

