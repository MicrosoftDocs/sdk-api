---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetStreamAttribute
title: IMFMediaEngineEx::GetStreamAttribute (mfmediaengine.h)
description: Gets a stream-level attribute from the media resource.
helpviewer_keywords: ["GetStreamAttribute","GetStreamAttribute method [Media Foundation]","GetStreamAttribute method [Media Foundation]","IMFMediaEngineEx interface","IMFMediaEngineEx interface [Media Foundation]","GetStreamAttribute method","IMFMediaEngineEx.GetStreamAttribute","IMFMediaEngineEx::GetStreamAttribute","mf.imfmediaengineex_getstreamattribute","mfmediaengine/IMFMediaEngineEx::GetStreamAttribute"]
old-location: mf\imfmediaengineex_getstreamattribute.htm
tech.root: mf
ms.assetid: 2C64CD7B-F376-47DF-AD5A-DE5EBC665288
ms.date: 12/05/2018
ms.keywords: GetStreamAttribute, GetStreamAttribute method [Media Foundation], GetStreamAttribute method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetStreamAttribute method, IMFMediaEngineEx.GetStreamAttribute, IMFMediaEngineEx::GetStreamAttribute, mf.imfmediaengineex_getstreamattribute, mfmediaengine/IMFMediaEngineEx::GetStreamAttribute
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
 - IMFMediaEngineEx::GetStreamAttribute
 - mfmediaengine/IMFMediaEngineEx::GetStreamAttribute
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
 - IMFMediaEngineEx.GetStreamAttribute
---

# IMFMediaEngineEx::GetStreamAttribute


## -description

Gets a stream-level attribute from the media resource.

## -parameters

### -param dwStreamIndex [in]

The zero-based index of the stream. To get the number of streams, call <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-getnumberofstreams">IMFMediaEngineEx::GetNumberOfStreams</a>.

### -param guidMFAttribute [in]

The attribute to query. Possible values are listed in the following topics:


<ul>
<li>
<a href="/windows/desktop/medfound/stream-descriptor-attributes">Stream Descriptor Attributes</a>
</li>
<li>
<a href="/windows/desktop/medfound/media-type-attributes">Media Type Attributes</a>
</li>
</ul>

### -param pvValue [out]

A pointer to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> that receives the value. The method fills the <b>PROPVARIANT</b> with a copy of the stored value. Call <a href="/windows/desktop/api/propidl/nf-propidl-propvariantclear">PropVariantClear</a> to free the memory allocated by the method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>