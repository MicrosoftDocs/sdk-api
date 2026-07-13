---
UID: NF:mfmediaengine.IMFMediaTimeRange.AddRange
title: IMFMediaTimeRange::AddRange (mfmediaengine.h)
description: Adds a new range to the list of time ranges.
helpviewer_keywords: ["AddRange","AddRange method [Media Foundation]","AddRange method [Media Foundation]","IMFMediaTimeRange interface","IMFMediaTimeRange interface [Media Foundation]","AddRange method","IMFMediaTimeRange.AddRange","IMFMediaTimeRange::AddRange","mf.imfmediatimerange_addrange","mfmediaengine/IMFMediaTimeRange::AddRange"]
old-location: mf\imfmediatimerange_addrange.htm
tech.root: mf
ms.assetid: 6BA36A44-78AC-4868-9E6A-601C0740E67A
ms.date: 12/05/2018
ms.keywords: AddRange, AddRange method [Media Foundation], AddRange method [Media Foundation],IMFMediaTimeRange interface, IMFMediaTimeRange interface [Media Foundation],AddRange method, IMFMediaTimeRange.AddRange, IMFMediaTimeRange::AddRange, mf.imfmediatimerange_addrange, mfmediaengine/IMFMediaTimeRange::AddRange
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
 - IMFMediaTimeRange::AddRange
 - mfmediaengine/IMFMediaTimeRange::AddRange
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
 - IMFMediaTimeRange.AddRange
---

# IMFMediaTimeRange::AddRange


## -description

Adds a new range to the list of time ranges.

## -parameters

### -param startTime [in]

The start time, in seconds.

### -param endTime [in]

The end time, in seconds.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the new range intersects a range already in the list, the two ranges are combined. Otherwise, the new range is added to the list.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediatimerange">IMFMediaTimeRange</a>