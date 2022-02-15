---
UID: NF:msrdc.ISimilarityTraitsTable.FindSimilarFileIndex
title: ISimilarityTraitsTable::FindSimilarFileIndex (msrdc.h)
description: Returns a list of files that are similar to a given file. The results in the list are sorted in order of similarity, beginning with the most similar file.
helpviewer_keywords: ["FindSimilarFileIndex","FindSimilarFileIndex method [Remote Differential Compression]","FindSimilarFileIndex method [Remote Differential Compression]","ISimilarityTraitsTable interface","ISimilarityTraitsTable interface [Remote Differential Compression]","FindSimilarFileIndex method","ISimilarityTraitsTable.FindSimilarFileIndex","ISimilarityTraitsTable::FindSimilarFileIndex","fs.isimilaritytraitstable_findsimilarfileindex","msrdc/ISimilarityTraitsTable::FindSimilarFileIndex","rdc.isimilaritytraitstable_findsimilarfileindex"]
old-location: rdc\isimilaritytraitstable_findsimilarfileindex.htm
tech.root: rdc
ms.assetid: 09c9b918-1def-4d19-84d4-99b881070e36
ms.date: 12/05/2018
ms.keywords: FindSimilarFileIndex, FindSimilarFileIndex method [Remote Differential Compression], FindSimilarFileIndex method [Remote Differential Compression],ISimilarityTraitsTable interface, ISimilarityTraitsTable interface [Remote Differential Compression],FindSimilarFileIndex method, ISimilarityTraitsTable.FindSimilarFileIndex, ISimilarityTraitsTable::FindSimilarFileIndex, fs.isimilaritytraitstable_findsimilarfileindex, msrdc/ISimilarityTraitsTable::FindSimilarFileIndex, rdc.isimilaritytraitstable_findsimilarfileindex
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISimilarityTraitsTable::FindSimilarFileIndex
 - msrdc/ISimilarityTraitsTable::FindSimilarFileIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - ISimilarityTraitsTable.FindSimilarFileIndex
---

# ISimilarityTraitsTable::FindSimilarFileIndex


## -description

Returns a list of files that are similar to a given file. The results in the list are sorted in order of similarity, beginning with the most similar file.

## -parameters

### -param similarityData [in]

A pointer to a <a href="/windows/win32/api/msrdc/ns-msrdc-similaritydata">SimilarityData</a> structure that contains similarity information for the file.

### -param numberOfMatchesRequired

TBD

### -param findSimilarFileIndexResults [out]

A pointer to a buffer that receives an array of <a href="/windows/win32/api/msrdc/ns-msrdc-findsimilarfileindexresults">FindSimilarFileIndexResults</a> structures that contain the requested information.

### -param resultsSize [in]

The number of <a href="/windows/win32/api/msrdc/ns-msrdc-findsimilarfileindexresults">FindSimilarFileIndexResults</a> structures that can be stored in the buffer that the <i>findSimilarFileIndexResults</i> parameter points to.

### -param resultsUsed [out]

The number of <a href="/windows/win32/api/msrdc/ns-msrdc-findsimilarfileindexresults">FindSimilarFileIndexResults</a> structures that were returned in the buffer that the <i>findSimilarFileIndexResults</i> parameter points to.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The list of files that is returned in the <i>findSimilarFileIndexResults</i> parameter may include files that have been deleted.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitstable">ISimilarityTraitsTable</a>