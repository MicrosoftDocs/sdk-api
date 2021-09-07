---
UID: NF:mfidl.MFCreateMuxSink
title: MFCreateMuxSink function (mfidl.h)
description: Creates a generic media sink that wraps a multiplexer Microsoft Media Foundation transform (MFT).
helpviewer_keywords: ["MFCreateMuxSink","MFCreateMuxSink function [Media Foundation]","mf.mfcreatemuxsink","mfidl/MFCreateMuxSink"]
old-location: mf\mfcreatemuxsink.htm
tech.root: mf
ms.assetid: 31A8790B-4C71-4D0D-B686-27B345745872
ms.date: 12/05/2018
ms.keywords: MFCreateMuxSink, MFCreateMuxSink function [Media Foundation], mf.mfcreatemuxsink, mfidl/MFCreateMuxSink
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateMuxSink
 - mfidl/MFCreateMuxSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateMuxSink
---

# MFCreateMuxSink function


## -description

Creates a generic media sink that wraps a multiplexer Microsoft Media Foundation transform (MFT).

## -parameters

### -param guidOutputSubType [in]

The subtype GUID of the output type for the MFT.

### -param pOutputAttributes [in]

A list of format attributes for the MFT output type. This parameter is optional and can be <b>NULL</b>.

### -param pOutputByteStream [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface of a byte stream. The output from the MFT is written to this byte stream. This parameter can be <b>NULL</b>.

### -param ppMuxSink [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a> interface of the media sink. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function attempts to find a multiplexer MFT that supports an output type with the following definition:

<ul>
<li>Major type: <b>MFMediaType_Stream</b></li>
<li>Subtype: <i>guidOutputSubType</i></li>
<li>Additional format attributes (optional)</li>
</ul>
To provide a list of additional format attributes:

<ol>
<li>Call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes">MFCreateAttributes</a> to get an <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> pointer.</li>
<li>Use the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface to set the attributes. (See <a href="/windows/desktop/medfound/media-type-attributes">Media Type Attributes</a>.)</li>
<li>Pass the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> pointer in the <i>pOutputAttributes</i> parameter.</li>
</ol>
The multiplexer MFT must be registered in the <a href="/windows/desktop/medfound/mft-category">MFT_CATEGORY_MULTIPLEXER</a>  category.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>