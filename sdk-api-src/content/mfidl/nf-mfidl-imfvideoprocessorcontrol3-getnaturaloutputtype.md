---
UID: NF:mfidl.IMFVideoProcessorControl3.GetNaturalOutputType
tech.root: mf
title: IMFVideoProcessorControl3::GetNaturalOutputType
ms.date: 09/09/2025
targetos: Windows
description: For a given input type, returns the "natural output type" of the video.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mfidl.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 version 1803
req.target-min-winversvr: Windows Server version 1803
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFVideoProcessorControl3::GetNaturalOutputType
f1_keywords:
 - IMFVideoProcessorControl3::GetNaturalOutputType
 - mfidl/IMFVideoProcessorControl3::GetNaturalOutputType
dev_langs:
 - c++
helpviewer_keywords:
 - GetNaturalOutputType
---

## -description

For a given input type, returns the "natural output type" of the video.


## -parameters

### -param ppType [out]

A pointer to an [IMFMediaType](/windows/win32/api/mfobjects/nn-mfobjects-imfmediatype) object specifying the natural output type of the video.

## -returns

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

The natural type is defined as:

* No scaling is applied
* No color conversions are applied

This accounts for any rotation, cropping, or pixel aspect applied to the video.

## -see-also

