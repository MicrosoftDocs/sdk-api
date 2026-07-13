---
UID: NF:mfapi.MFCombineSamples
title: MFCombineSamples
ms.date: 11/4/2019
targetos: Windows
description: Concatenates a media sample onto another sample if their combined duration does not exceed the specified duration.
tech.root: mf
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mfapi.h
req.idl: Mfplat.dll
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Mfplat.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mfplat.dll
api_name:
 - MFCombineSamples
f1_keywords:
 - MFCombineSamples
 - mfapi/MFCombineSamples
dev_langs:
 - c++
---

## -description

Concatenates a media sample onto another sample if their combined duration does not exceed the specified duration.

## -parameters

### -param pSample

A pointer to an [IMFSample](../mfobjects/nn-mfobjects-imfsample.md) to which the sample provided in the *pSampleToAdd* parameter is appended.

### -param pSampleToAdd

A pointer to an [IMFSample](../mfobjects/nn-mfobjects-imfsample.md) to append to the sample provided in the  *pSample* parameter.

### -param dwMaxMergedDurationInMS

The maximum duration in milliseconds that the combined sample can fill for the operation to be successful.

### -param pMerged

Output parameter that receives a BOOL indicating whether the sample was successfully appended.

## -returns

Returns HRESULT.

## -remarks

Split combined samples by calling [MFSplitSample](nf-mfapi-mfsplitsample.md)

## -see-also