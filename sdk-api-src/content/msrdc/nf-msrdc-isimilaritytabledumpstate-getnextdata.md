---
UID: NF:msrdc.ISimilarityTableDumpState.GetNextData
title: ISimilarityTableDumpState::GetNextData (msrdc.h)
description: Retrieves one or more SimilarityDumpData structures from the similarity traits list that was returned by the ISimilarityTraitsTable::BeginDump method.
helpviewer_keywords: ["GetNextData","GetNextData method [Remote Differential Compression]","GetNextData method [Remote Differential Compression]","ISimilarityTableDumpState interface","ISimilarityTableDumpState interface [Remote Differential Compression]","GetNextData method","ISimilarityTableDumpState.GetNextData","ISimilarityTableDumpState::GetNextData","fs.isimilaritytabledumpstate_getnextdata","msrdc/ISimilarityTableDumpState::GetNextData","rdc.isimilaritytabledumpstate_getnextdata"]
old-location: rdc\isimilaritytabledumpstate_getnextdata.htm
tech.root: rdc
ms.assetid: 40ec97fc-052d-474e-9a55-822aa113ac03
ms.date: 12/05/2018
ms.keywords: GetNextData, GetNextData method [Remote Differential Compression], GetNextData method [Remote Differential Compression],ISimilarityTableDumpState interface, ISimilarityTableDumpState interface [Remote Differential Compression],GetNextData method, ISimilarityTableDumpState.GetNextData, ISimilarityTableDumpState::GetNextData, fs.isimilaritytabledumpstate_getnextdata, msrdc/ISimilarityTableDumpState::GetNextData, rdc.isimilaritytabledumpstate_getnextdata
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
 - ISimilarityTableDumpState::GetNextData
 - msrdc/ISimilarityTableDumpState::GetNextData
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
 - ISimilarityTableDumpState.GetNextData
---

# ISimilarityTableDumpState::GetNextData


## -description

Retrieves one or more <a href="/windows/win32/api/msrdc/ns-msrdc-similaritydumpdata">SimilarityDumpData</a> structures from the similarity traits list that was returned by the <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilaritytraitstable-begindump">ISimilarityTraitsTable::BeginDump</a> method.

## -parameters

### -param resultsSize [in]

The number of <a href="/windows/win32/api/msrdc/ns-msrdc-similaritydumpdata">SimilarityDumpData</a> structures that can be stored in the buffer that the <i>results</i> parameter points to.

### -param resultsUsed [out]

A pointer to a variable that receives the number of <a href="/windows/win32/api/msrdc/ns-msrdc-similaritydumpdata">SimilarityDumpData</a> structures that were returned in the buffer that the <i>results</i> parameter points to.

### -param eof [out]

A pointer to a variable that receives <b>TRUE</b> if the end of the file is reached; otherwise, <b>FALSE</b>.

### -param results [in, out]

A pointer to a buffer that receives the <a href="/windows/win32/api/msrdc/ns-msrdc-similaritydumpdata">SimilarityDumpData</a> structures.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytabledumpstate">ISimilarityTableDumpState</a>