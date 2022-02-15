---
UID: NF:mfmediaengine.IMFMediaTimeRange.GetStart
title: IMFMediaTimeRange::GetStart (mfmediaengine.h)
description: Gets the start time for a specified time range.
helpviewer_keywords: ["GetStart","GetStart method [Media Foundation]","GetStart method [Media Foundation]","IMFMediaTimeRange interface","IMFMediaTimeRange interface [Media Foundation]","GetStart method","IMFMediaTimeRange.GetStart","IMFMediaTimeRange::GetStart","mf.imfmediatimerange_getstart","mfmediaengine/IMFMediaTimeRange::GetStart"]
old-location: mf\imfmediatimerange_getstart.htm
tech.root: mf
ms.assetid: E02CFE99-78B8-4923-8922-467A55442802
ms.date: 12/05/2018
ms.keywords: GetStart, GetStart method [Media Foundation], GetStart method [Media Foundation],IMFMediaTimeRange interface, IMFMediaTimeRange interface [Media Foundation],GetStart method, IMFMediaTimeRange.GetStart, IMFMediaTimeRange::GetStart, mf.imfmediatimerange_getstart, mfmediaengine/IMFMediaTimeRange::GetStart
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaTimeRange::GetStart
 - mfmediaengine/IMFMediaTimeRange::GetStart
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaTimeRange.GetStart
---

# IMFMediaTimeRange::GetStart


## -description

Gets the start time for a specified time range.

## -parameters

### -param index [in]

The zero-based index of the time range to query. To get the  number of time ranges, call <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediatimerange-getlength">IMFMediaTimeRange::GetLength</a>.

### -param pStart [out]

Receives the start time, in seconds.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method corresponds to the <b>TimeRanges.start</b> method in HTML5.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediatimerange">IMFMediaTimeRange</a>