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

# ISimilarityTableDumpState::GetNextData


## -description


Retrieves one or more <a href="https://msdn.microsoft.com/0200008c-5664-445f-ae65-0eb004856a4c">SimilarityDumpData</a> structures from the similarity traits list that was returned by the <a href="https://msdn.microsoft.com/93298019-334b-4685-b95e-a1081c2bd9dc">ISimilarityTraitsTable::BeginDump</a> method.


## -parameters




### -param resultsSize [in]

The number of <a href="https://msdn.microsoft.com/0200008c-5664-445f-ae65-0eb004856a4c">SimilarityDumpData</a> structures that can be stored in the buffer that the <i>results</i> parameter points to.


### -param resultsUsed [out]

A pointer to a variable that receives the number of <a href="https://msdn.microsoft.com/0200008c-5664-445f-ae65-0eb004856a4c">SimilarityDumpData</a> structures that were returned in the buffer that the <i>results</i> parameter points to.


### -param eof [out]

A pointer to a variable that receives <b>TRUE</b> if the end of the file is reached; otherwise, <b>FALSE</b>.


### -param results [in, out]

A pointer to a buffer that receives the <a href="https://msdn.microsoft.com/0200008c-5664-445f-ae65-0eb004856a4c">SimilarityDumpData</a> structures.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a56433b5-191f-49fe-83fb-7057e4c30bbd">ISimilarityTableDumpState</a>
 

 

