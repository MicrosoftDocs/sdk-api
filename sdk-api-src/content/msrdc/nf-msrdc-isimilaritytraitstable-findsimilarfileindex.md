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

# ISimilarityTraitsTable::FindSimilarFileIndex


## -description


Returns a list of files that are similar to a given file. The results in the list are sorted in order of similarity, beginning with the most similar file.


## -parameters




### -param similarityData [in]

A pointer to a <a href="https://msdn.microsoft.com/33fdb48c-6f33-44e8-83b1-6029b1eace1d">SimilarityData</a> structure that contains similarity information for the file.


### -param numberOfMatchesRequired




### -param findSimilarFileIndexResults [out]

A pointer to a buffer that receives an array of <a href="https://msdn.microsoft.com/2e0d39ab-d491-496e-8753-e7223a5c5029">FindSimilarFileIndexResults</a> structures that contain the requested information.


### -param resultsSize [in]

The number of <a href="https://msdn.microsoft.com/2e0d39ab-d491-496e-8753-e7223a5c5029">FindSimilarFileIndexResults</a> structures that can be stored in the buffer that the <i>findSimilarFileIndexResults</i> parameter points to.


### -param resultsUsed [out]

The number of <a href="https://msdn.microsoft.com/2e0d39ab-d491-496e-8753-e7223a5c5029">FindSimilarFileIndexResults</a> structures that were returned in the buffer that the <i>findSimilarFileIndexResults</i> parameter points to.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The list of files that is returned in the <i>findSimilarFileIndexResults</i> parameter may include files that have been deleted.




## -see-also




<a href="https://msdn.microsoft.com/0985e27c-aa70-43c1-bcec-00ef14f2df58">ISimilarityTraitsTable</a>
 

 

