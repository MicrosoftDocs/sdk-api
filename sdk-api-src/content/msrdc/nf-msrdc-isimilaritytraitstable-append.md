---
UID: NF:msrdc.ISimilarityTraitsTable.Append
title: ISimilarityTraitsTable::Append (msrdc.h)
description: Adds a SimilarityData structure to the similarity traits table.
helpviewer_keywords: ["Append","Append method [Remote Differential Compression]","Append method [Remote Differential Compression]","ISimilarityTraitsTable interface","ISimilarityTraitsTable interface [Remote Differential Compression]","Append method","ISimilarityTraitsTable.Append","ISimilarityTraitsTable::Append","fs.isimilaritytraitstable_append","msrdc/ISimilarityTraitsTable::Append","rdc.isimilaritytraitstable_append"]
old-location: rdc\isimilaritytraitstable_append.htm
tech.root: rdc
ms.assetid: e4c5f75c-282e-4c99-8c5a-53421f4bfc92
ms.date: 12/05/2018
ms.keywords: Append, Append method [Remote Differential Compression], Append method [Remote Differential Compression],ISimilarityTraitsTable interface, ISimilarityTraitsTable interface [Remote Differential Compression],Append method, ISimilarityTraitsTable.Append, ISimilarityTraitsTable::Append, fs.isimilaritytraitstable_append, msrdc/ISimilarityTraitsTable::Append, rdc.isimilaritytraitstable_append
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
 - ISimilarityTraitsTable::Append
 - msrdc/ISimilarityTraitsTable::Append
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
 - ISimilarityTraitsTable.Append
---

# ISimilarityTraitsTable::Append


## -description

Adds a <a href="/windows/win32/api/msrdc/ns-msrdc-similaritydata">SimilarityData</a> structure to the similarity traits table.

## -parameters

### -param data [in]

The <a href="/windows/win32/api/msrdc/ns-msrdc-similaritydata">SimilarityData</a> structure to be added to the similarity traits table.

### -param fileIndex [in]

The index in the similarity traits table where the <a href="/windows/win32/api/msrdc/ns-msrdc-similaritydata">SimilarityData</a> structure is to be inserted.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The application must supply <i>fileIndex</i> values that are greater than zero and are always increasing. Otherwise, this method returns the <b>E_INVALIDARG</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitstable">ISimilarityTraitsTable</a>