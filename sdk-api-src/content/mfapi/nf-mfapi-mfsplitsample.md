---
UID: NF:mfapi.MFSplitSample
title: MFSplitSample
ms.date: 11/4/2019
targetos: Windows
description: Split up a combined media sample back into individual samples.
tech.root: mf
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Mfplat.dll
req.header: mfapi.h
req.idl: 
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
 - apiref
api_type:
 - DllExport
 - kbSyntax
api_location:
 - Mfplat.dll
api_name:
 - MFSplitSample
f1_keywords:
 - MFSplitSample
 - mfapi/MFSplitSample
dev_langs:
 - c++
---

## -description

Split up a combined media sample back into individual samples.

## -parameters

### -param pSample

A pointer to an [IMFSample](../mfobjects/nn-mfobjects-imfsample.md) representing a combined sample to be split.

### -param pOutputSamples

Receives a pointer to an array of output samples from the split operation.

### -param dwOutputSampleMaxCount

The maximum output array size. Call [IMFSample::GetBufferCount](../mfobjects/nf-mfobjects-imfsample-getbuffercount.md) on the sample provided in *pSample* to find out an upper bound.

### -param pdwOutputSampleCount

Output parameter that receives the number of samples contained in the pOutputSamples array.

## -returns

## -remarks

Combine samples by calling [MFCombineSamples](nf-mfapi-mfsplitsample.md)

## -see-also