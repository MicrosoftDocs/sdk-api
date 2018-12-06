---
UID: NF:msrdc.ISimilarityTraitsTable.FindSimilarFileIndex
title: ISimilarityTraitsTable::FindSimilarFileIndex
author: windows-sdk-content
description: Returns a list of files that are similar to a given file. The results in the list are sorted in order of similarity, beginning with the most similar file.
old-location: rdc\isimilaritytraitstable_findsimilarfileindex.htm
tech.root: rdc
ms.assetid: 09c9b918-1def-4d19-84d4-99b881070e36
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FindSimilarFileIndex, FindSimilarFileIndex method [Remote Differential Compression], FindSimilarFileIndex method [Remote Differential Compression],ISimilarityTraitsTable interface, ISimilarityTraitsTable interface [Remote Differential Compression],FindSimilarFileIndex method, ISimilarityTraitsTable.FindSimilarFileIndex, ISimilarityTraitsTable::FindSimilarFileIndex, fs.isimilaritytraitstable_findsimilarfileindex, msrdc/ISimilarityTraitsTable::FindSimilarFileIndex, rdc.isimilaritytraitstable_findsimilarfileindex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: MsRdc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - ISimilarityTraitsTable.FindSimilarFileIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISimilarityTraitsTable::FindSimilarFileIndex


## -description


Returns a list of files that are similar to a given file. The results in the list are sorted in order of similarity, beginning with the most similar file.


## -parameters




### -param similarityData [in]

A pointer to a <a href="https://msdn.microsoft.com/33fdb48c-6f33-44e8-83b1-6029b1eace1d">SimilarityData</a> structure that contains similarity information for the file.


### -param numberOfMatchesRequired

TBD


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
 

 

