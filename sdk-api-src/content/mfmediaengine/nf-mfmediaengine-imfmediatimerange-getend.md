---
UID: NF:mfmediaengine.IMFMediaTimeRange.GetEnd
title: IMFMediaTimeRange::GetEnd (mfmediaengine.h)
description: Gets the end time for a specified time range.
helpviewer_keywords: ["GetEnd","GetEnd method [Media Foundation]","GetEnd method [Media Foundation]","IMFMediaTimeRange interface","IMFMediaTimeRange interface [Media Foundation]","GetEnd method","IMFMediaTimeRange.GetEnd","IMFMediaTimeRange::GetEnd","mf.imfmediatimerange_getend","mfmediaengine/IMFMediaTimeRange::GetEnd"]
old-location: mf\imfmediatimerange_getend.htm
tech.root: mf
ms.assetid: 864C0DEE-A1F7-488C-9A9D-366602667DE9
ms.date: 12/05/2018
ms.keywords: GetEnd, GetEnd method [Media Foundation], GetEnd method [Media Foundation],IMFMediaTimeRange interface, IMFMediaTimeRange interface [Media Foundation],GetEnd method, IMFMediaTimeRange.GetEnd, IMFMediaTimeRange::GetEnd, mf.imfmediatimerange_getend, mfmediaengine/IMFMediaTimeRange::GetEnd
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
 - IMFMediaTimeRange::GetEnd
 - mfmediaengine/IMFMediaTimeRange::GetEnd
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
 - IMFMediaTimeRange.GetEnd
---

# IMFMediaTimeRange::GetEnd


## -description

Gets the end time for a specified time range.

## -parameters

### -param index [in]

The zero-based index of the time range to query. To get the  number of time ranges, call <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediatimerange-getlength">IMFMediaTimeRange::GetLength</a>.

### -param pEnd [out]

Receives the end time, in seconds.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method corresponds to the <b>TimeRanges.end</b> method in HTML5.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediatimerange">IMFMediaTimeRange</a>