---
UID: NF:msrdc.IFindSimilarResults.GetNextFileId
title: IFindSimilarResults::GetNextFileId (msrdc.h)
description: Retrieves the next valid similarity file ID in the file list that was returned by the ISimilarity::FindSimilarFileId method.
helpviewer_keywords: ["GetNextFileId","GetNextFileId method [Remote Differential Compression]","GetNextFileId method [Remote Differential Compression]","IFindSimilarResults interface","IFindSimilarResults interface [Remote Differential Compression]","GetNextFileId method","IFindSimilarResults.GetNextFileId","IFindSimilarResults::GetNextFileId","fs.ifindsimilarresults_getnextfileid","msrdc/IFindSimilarResults::GetNextFileId","rdc.ifindsimilarresults_getnextfileid"]
old-location: rdc\ifindsimilarresults_getnextfileid.htm
tech.root: rdc
ms.assetid: 881e0ae6-311f-4bc4-9660-b0e96b7b9bd2
ms.date: 12/05/2018
ms.keywords: GetNextFileId, GetNextFileId method [Remote Differential Compression], GetNextFileId method [Remote Differential Compression],IFindSimilarResults interface, IFindSimilarResults interface [Remote Differential Compression],GetNextFileId method, IFindSimilarResults.GetNextFileId, IFindSimilarResults::GetNextFileId, fs.ifindsimilarresults_getnextfileid, msrdc/IFindSimilarResults::GetNextFileId, rdc.ifindsimilarresults_getnextfileid
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
 - IFindSimilarResults::GetNextFileId
 - msrdc/IFindSimilarResults::GetNextFileId
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
 - IFindSimilarResults.GetNextFileId
---

# IFindSimilarResults::GetNextFileId


## -description

Retrieves the next valid similarity file ID in the file list that was returned by the <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarity-findsimilarfileid">ISimilarity::FindSimilarFileId</a> method.

## -parameters

### -param numTraitsMatched [out]

A pointer to a variable that receives the number of traits that were matched.

### -param similarityFileId [out]

A pointer to a <a href="/windows/win32/api/msrdc/ns-msrdc-similarityfileid">SimilarityFileId</a> structure that contains the similarity file ID of the matching file.

## -returns

Returns <b>S_OK</b> on success, or an error <b>HRESULT</b> on failure.

This method can also return the following error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-ifindsimilarresults">IFindSimilarResults</a>