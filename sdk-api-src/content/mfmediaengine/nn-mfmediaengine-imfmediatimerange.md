---
UID: NN:mfmediaengine.IMFMediaTimeRange
title: IMFMediaTimeRange (mfmediaengine.h)
description: Represents a list of time ranges, where each range is defined by a start and end time.
helpviewer_keywords: ["IMFMediaTimeRange","IMFMediaTimeRange interface [Media Foundation]","IMFMediaTimeRange interface [Media Foundation]","described","mf.imfmediatimerange","mfmediaengine/IMFMediaTimeRange"]
old-location: mf\imfmediatimerange.htm
tech.root: mf
ms.assetid: E39646E6-66F4-4413-A84B-43039689AEE7
ms.date: 12/05/2018
ms.keywords: IMFMediaTimeRange, IMFMediaTimeRange interface [Media Foundation], IMFMediaTimeRange interface [Media Foundation],described, mf.imfmediatimerange, mfmediaengine/IMFMediaTimeRange
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
 - IMFMediaTimeRange
 - mfmediaengine/IMFMediaTimeRange
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
 - IMFMediaTimeRange
---

# IMFMediaTimeRange interface


## -description

Represents a list of time ranges, where each range is defined by a start and end time.

## -inheritance

The <b>IMFMediaTimeRange</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaTimeRange</b> also has these types of members:

## -remarks

The <b>IMFMediaTimeRange</b> interface corresponds to the <b>TimeRanges</b> interface in HTML5.

Several <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a> methods return <b>IMFMediaTimeRange</b> pointers.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
