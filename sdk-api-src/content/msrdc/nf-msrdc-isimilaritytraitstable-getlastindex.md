---
UID: NF:msrdc.ISimilarityTraitsTable.GetLastIndex
title: ISimilarityTraitsTable::GetLastIndex (msrdc.h)
description: Retrieves the index of the last entry that was stored in the similarity traits table.
helpviewer_keywords: ["GetLastIndex","GetLastIndex method [Remote Differential Compression]","GetLastIndex method [Remote Differential Compression]","ISimilarityTraitsTable interface","ISimilarityTraitsTable interface [Remote Differential Compression]","GetLastIndex method","ISimilarityTraitsTable.GetLastIndex","ISimilarityTraitsTable::GetLastIndex","fs.isimilaritytraitstable_getlastindex","msrdc/ISimilarityTraitsTable::GetLastIndex","rdc.isimilaritytraitstable_getlastindex"]
old-location: rdc\isimilaritytraitstable_getlastindex.htm
tech.root: rdc
ms.assetid: 4e6cb7b4-0dcf-4a51-acf9-3263d73eee63
ms.date: 12/05/2018
ms.keywords: GetLastIndex, GetLastIndex method [Remote Differential Compression], GetLastIndex method [Remote Differential Compression],ISimilarityTraitsTable interface, ISimilarityTraitsTable interface [Remote Differential Compression],GetLastIndex method, ISimilarityTraitsTable.GetLastIndex, ISimilarityTraitsTable::GetLastIndex, fs.isimilaritytraitstable_getlastindex, msrdc/ISimilarityTraitsTable::GetLastIndex, rdc.isimilaritytraitstable_getlastindex
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
 - ISimilarityTraitsTable::GetLastIndex
 - msrdc/ISimilarityTraitsTable::GetLastIndex
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
 - ISimilarityTraitsTable.GetLastIndex
---

# ISimilarityTraitsTable::GetLastIndex


## -description

Retrieves the index of the last entry that was stored in the similarity traits table.

## -parameters

### -param fileIndex [out]

A pointer to a variable that receives the index of the last entry.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitstable">ISimilarityTraitsTable</a>