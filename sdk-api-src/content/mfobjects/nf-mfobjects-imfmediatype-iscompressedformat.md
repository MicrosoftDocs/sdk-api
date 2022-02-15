---
UID: NF:mfobjects.IMFMediaType.IsCompressedFormat
title: IMFMediaType::IsCompressedFormat (mfobjects.h)
description: Queries whether the media type is a temporally compressed format.
helpviewer_keywords: ["IMFMediaType interface [Media Foundation]","IsCompressedFormat method","IMFMediaType.IsCompressedFormat","IMFMediaType::IsCompressedFormat","IsCompressedFormat","IsCompressedFormat method [Media Foundation]","IsCompressedFormat method [Media Foundation]","IMFMediaType interface","d15d683b-f2ce-40ac-9724-a0785f5d335c","mf.imfmediatype_iscompressedformat","mfobjects/IMFMediaType::IsCompressedFormat"]
old-location: mf\imfmediatype_iscompressedformat.htm
tech.root: mf
ms.assetid: d15d683b-f2ce-40ac-9724-a0785f5d335c
ms.date: 12/05/2018
ms.keywords: IMFMediaType interface [Media Foundation],IsCompressedFormat method, IMFMediaType.IsCompressedFormat, IMFMediaType::IsCompressedFormat, IsCompressedFormat, IsCompressedFormat method [Media Foundation], IsCompressedFormat method [Media Foundation],IMFMediaType interface, d15d683b-f2ce-40ac-9724-a0785f5d335c, mf.imfmediatype_iscompressedformat, mfobjects/IMFMediaType::IsCompressedFormat
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaType::IsCompressedFormat
 - mfobjects/IMFMediaType::IsCompressedFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaType.IsCompressedFormat
---

# IMFMediaType::IsCompressedFormat


## -description

Queries whether the media type is a temporally compressed format.Temporal compression uses information from previously decoded samples when decompressing the current sample.

## -parameters

### -param pfCompressed [out]

Receives a Boolean value. The value is <b>TRUE</b> if the format uses temporal compression, or <b>FALSE</b> if the format does not use temporal compression.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method returns <b>FALSE</b> in <i>pfCompressed</i> if the media type's <a href="/windows/desktop/medfound/mf-mt-all-samples-independent-attribute">MF_MT_ALL_SAMPLES_INDEPENDENT</a> attribute is <b>TRUE</b>. If the <b>MF_MT_ALL_SAMPLES_INDEPENDENT</b> attribute is <b>FALSE</b> or not set, the method returns <b>TRUE</b>.
      

If the method returns <b>TRUE</b> in <i>pfCompressed</i>, it is a hint that the format has temporal compression applied to it. If the method returns <b>FALSE</b>, the format does not use temporal compression, although it might use intra-frame compression.
      

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>