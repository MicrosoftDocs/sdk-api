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

# ISimilarity::FindSimilarFileId


## -description


Returns a list of files that are similar to a given file.


## -parameters




### -param similarityData [in]

A pointer to a <a href="https://msdn.microsoft.com/33fdb48c-6f33-44e8-83b1-6029b1eace1d">SimilarityData</a> structure that contains similarity information for the file.


### -param numberOfMatchesRequired




### -param resultsSize [in]

The number of file IDs that can be stored in the <a href="https://msdn.microsoft.com/3118cf53-c544-48bc-ac38-79ca2252f83f">IFindSimilarResults</a> object that the <i>findSimilarResults</i> parameter points to.


### -param findSimilarResults [out, optional]

A pointer to a location that will receive the returned  <a href="https://msdn.microsoft.com/3118cf53-c544-48bc-ac38-79ca2252f83f">IFindSimilarResults</a> interface pointer. The caller must release this interface when it is no longer needed.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The file IDs that are returned in the <i>findSimilarResults</i> parameter may include IDs of files that have been deleted.




## -see-also




<a href="https://msdn.microsoft.com/fe0cd874-a40c-4d82-99bf-b84008a4995c">ISimilarity</a>
 

 

