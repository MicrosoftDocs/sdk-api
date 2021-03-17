---
UID: NS:msrdc.__MIDL___MIDL_itf_msrdc_0000_0000_0014
title: SimilarityDumpData (msrdc.h)
description: Contains the similarity information that was returned for a file by the ISimilarityTableDumpState::GetNextData method.
helpviewer_keywords: ["SimilarityDumpData","SimilarityDumpData structure [Remote Differential Compression]","fs.similaritydumpdata","msrdc/SimilarityDumpData","rdc.similaritydumpdata"]
old-location: rdc\similaritydumpdata.htm
tech.root: rdc
ms.assetid: 0200008c-5664-445f-ae65-0eb004856a4c
ms.date: 12/05/2018
ms.keywords: SimilarityDumpData, SimilarityDumpData structure [Remote Differential Compression], fs.similaritydumpdata, msrdc/SimilarityDumpData, rdc.similaritydumpdata
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SimilarityDumpData
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msrdc_0000_0000_0014
 - msrdc/__MIDL___MIDL_itf_msrdc_0000_0000_0014
 - SimilarityDumpData
 - msrdc/SimilarityDumpData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - MsRdc.h
api_name:
 - SimilarityDumpData
---

# SimilarityDumpData structure


## -description

Contains the similarity information that was returned for a file by the <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilaritytabledumpstate-getnextdata">ISimilarityTableDumpState::GetNextData</a> method.

## -struct-fields

### -field m_FileIndex

The index of the <a href="/windows/win32/api/msrdc/ns-msrdc-similaritydata">SimilarityData</a> structure in the similarity traits table.

### -field m_Data

A <a href="/windows/win32/api/msrdc/ns-msrdc-similaritydata">SimilarityData</a> structure that contains the similarity data for the file.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytabledumpstate">ISimilarityTableDumpState</a>