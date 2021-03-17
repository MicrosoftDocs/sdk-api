---
UID: NF:msrdc.IFindSimilarResults.GetSize
title: IFindSimilarResults::GetSize (msrdc.h)
description: Retrieves the number of entries in the file list that was returned by the ISimilarity::FindSimilarFileId method.
helpviewer_keywords: ["GetSize","GetSize method [Remote Differential Compression]","GetSize method [Remote Differential Compression]","IFindSimilarResults interface","IFindSimilarResults interface [Remote Differential Compression]","GetSize method","IFindSimilarResults.GetSize","IFindSimilarResults::GetSize","fs.ifindsimilarresults_getsize","msrdc/IFindSimilarResults::GetSize","rdc.ifindsimilarresults_getsize"]
old-location: rdc\ifindsimilarresults_getsize.htm
tech.root: rdc
ms.assetid: c59a6fb0-e81f-4b7d-b0e6-9a5c9730fa9d
ms.date: 12/05/2018
ms.keywords: GetSize, GetSize method [Remote Differential Compression], GetSize method [Remote Differential Compression],IFindSimilarResults interface, IFindSimilarResults interface [Remote Differential Compression],GetSize method, IFindSimilarResults.GetSize, IFindSimilarResults::GetSize, fs.ifindsimilarresults_getsize, msrdc/IFindSimilarResults::GetSize, rdc.ifindsimilarresults_getsize
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
 - IFindSimilarResults::GetSize
 - msrdc/IFindSimilarResults::GetSize
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
 - IFindSimilarResults.GetSize
---

# IFindSimilarResults::GetSize


## -description

Retrieves the number of entries in the  file list that was returned by the <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarity-findsimilarfileid">ISimilarity::FindSimilarFileId</a> method.

The actual number of similarity file IDs that are returned by the <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-ifindsimilarresults-getnextfileid">GetNextFileId</a> method may be less than the number that is  returned by the <b>GetSize</b>  method.  <b>GetNextFileId</b> returns only valid similarity file IDs. However, <b>GetSize</b> counts all entries, even if their similarity file IDs are not valid.

## -parameters

### -param size [out]

A pointer to a variable that receives the number of entries in the file list.

## -returns

This method always returns <b>S_OK</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-ifindsimilarresults">IFindSimilarResults</a>