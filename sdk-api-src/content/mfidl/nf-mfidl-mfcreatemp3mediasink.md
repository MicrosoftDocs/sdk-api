---
UID: NF:mfidl.MFCreateMP3MediaSink
title: MFCreateMP3MediaSink function (mfidl.h)
description: Creates the MP3 media sink.
helpviewer_keywords: ["MFCreateMP3MediaSink","MFCreateMP3MediaSink function [Media Foundation]","mf.mfcreatemp3mediasink","mfidl/MFCreateMP3MediaSink"]
old-location: mf\mfcreatemp3mediasink.htm
tech.root: mf
ms.assetid: b555e9c8-5a2a-452d-8edf-c41c0e24296b
ms.date: 12/05/2018
ms.keywords: MFCreateMP3MediaSink, MFCreateMP3MediaSink function [Media Foundation], mf.mfcreatemp3mediasink, mfidl/MFCreateMP3MediaSink
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - MFCreateMP3MediaSink
 - mfidl/MFCreateMP3MediaSink
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
 - MFCreateMP3MediaSink
---

# MFCreateMP3MediaSink function


## -description

Creates the MP3 media sink.

## -parameters

### -param pTargetByteStream [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface of a byte stream.  The media sink writes the MP3 file to this byte stream. The byte stream must be writable.

### -param ppMediaSink [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a> interface of the MP3 media sink.. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The MP3  media sink takes compressed MP3
audio samples as input, and writes an MP3 file with ID3 headers as output. The MP3 media sink does not perform MP3 audio encoding.
      


#### Examples


```cpp
HRESULT CreateMP3Sink(PCWSTR pszOutputFile, IMFMediaSink **ppSink)
{
    *ppSink = NULL;

    IMFByteStream* pStream = NULL;

    // Create a byte stream for the output file.
    HRESULT hr =  MFCreateFile(
        MF_ACCESSMODE_WRITE, 
        MF_OPENMODE_DELETE_IF_EXIST, 
        MF_FILEFLAGS_NONE, 
        pszOutputFile, 
        &pStream
        );
       
    // Create the MP3 media sink.
    if (SUCCEEDED(hr))
    {
        hr =  MFCreateMP3MediaSink(pStream, ppSink);
    }

    SafeRelease(&pStream);
    return hr;
}

```

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>