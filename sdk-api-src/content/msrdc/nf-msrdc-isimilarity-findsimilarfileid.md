---
UID: NF:msrdc.ISimilarity.FindSimilarFileId
title: ISimilarity::FindSimilarFileId (msrdc.h)
description: Returns a list of files that are similar to a given file.
helpviewer_keywords: ["FindSimilarFileId","FindSimilarFileId method [Remote Differential Compression]","FindSimilarFileId method [Remote Differential Compression]","ISimilarity interface","ISimilarity interface [Remote Differential Compression]","FindSimilarFileId method","ISimilarity.FindSimilarFileId","ISimilarity::FindSimilarFileId","fs.isimilarity_findsimilarfileid","msrdc/ISimilarity::FindSimilarFileId","rdc.isimilarity_findsimilarfileid"]
old-location: rdc\isimilarity_findsimilarfileid.htm
tech.root: rdc
ms.assetid: 70a205fc-d90a-43fc-88f4-2f3a573c5a82
ms.date: 12/05/2018
ms.keywords: FindSimilarFileId, FindSimilarFileId method [Remote Differential Compression], FindSimilarFileId method [Remote Differential Compression],ISimilarity interface, ISimilarity interface [Remote Differential Compression],FindSimilarFileId method, ISimilarity.FindSimilarFileId, ISimilarity::FindSimilarFileId, fs.isimilarity_findsimilarfileid, msrdc/ISimilarity::FindSimilarFileId, rdc.isimilarity_findsimilarfileid
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
 - ISimilarity::FindSimilarFileId
 - msrdc/ISimilarity::FindSimilarFileId
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
 - ISimilarity.FindSimilarFileId
---

# ISimilarity::FindSimilarFileId


## -description

Returns a list of files that are similar to a given file.

## -parameters

### -param similarityData [in]

A pointer to a <a href="/windows/win32/api/msrdc/ns-msrdc-similaritydata">SimilarityData</a> structure that contains similarity information for the file.

### -param numberOfMatchesRequired

TBD

### -param resultsSize [in]

The number of file IDs that can be stored in the <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-ifindsimilarresults">IFindSimilarResults</a> object that the <i>findSimilarResults</i> parameter points to.

### -param findSimilarResults [out, optional]

A pointer to a location that will receive the returned  <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-ifindsimilarresults">IFindSimilarResults</a> interface pointer. The caller must release this interface when it is no longer needed.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The file IDs that are returned in the <i>findSimilarResults</i> parameter may include IDs of files that have been deleted.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilarity">ISimilarity</a>