---
UID: NF:dwrite_3.IDWriteFactory5.AnalyzeContainerType
title: IDWriteFactory5::AnalyzeContainerType (dwrite_3.h)
description: The AnalyzeContainerType method analyzes the specified file data to determine whether it is a known font container format (e.g., WOFF or WOFF2).
helpviewer_keywords: ["AnalyzeContainerType","AnalyzeContainerType method [Direct Write]","AnalyzeContainerType method [Direct Write]","IDWriteFactory5 interface","IDWriteFactory5 interface [Direct Write]","AnalyzeContainerType method","IDWriteFactory5.AnalyzeContainerType","IDWriteFactory5::AnalyzeContainerType","directwrite.idwritefactory5_analyzecontainertype","dwrite_3/IDWriteFactory5::AnalyzeContainerType"]
old-location: directwrite\idwritefactory5_analyzecontainertype.htm
tech.root: DirectWrite
ms.assetid: A13656C9-E793-40E2-81BD-0F9C0F437F1E
ms.date: 09/10/2025
ms.keywords: AnalyzeContainerType, AnalyzeContainerType method [Direct Write], AnalyzeContainerType method [Direct Write],IDWriteFactory5 interface, IDWriteFactory5 interface [Direct Write],AnalyzeContainerType method, IDWriteFactory5.AnalyzeContainerType, IDWriteFactory5::AnalyzeContainerType, directwrite.idwritefactory5_analyzecontainertype, dwrite_3/IDWriteFactory5::AnalyzeContainerType
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 15063
req.target-min-winversvr: Windows 10 Build 15063
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFactory5::AnalyzeContainerType
 - dwrite_3/IDWriteFactory5::AnalyzeContainerType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteFactory5.AnalyzeContainerType
---

# IDWriteFactory5::AnalyzeContainerType


## -description

The AnalyzeContainerType method analyzes the specified file data to determine whether it is a known font container format (e.g., WOFF or WOFF2).

## -parameters

### -param fileData [in]

Type: <b>void</b>

Pointer to the file data to analyze.

### -param fileDataSize

Type: <b>UINT32</b>

Size of the buffer passed in fileData.

## -returns

Type: <b><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_container_type">DWRITE_CONTAINER_TYPE</a></b>

Returns the container type if recognized. DWRITE_CONTAINER_TYPE_UNKOWNN is returned for all other files, including uncompressed font files.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5">IDWriteFactory5</a>

