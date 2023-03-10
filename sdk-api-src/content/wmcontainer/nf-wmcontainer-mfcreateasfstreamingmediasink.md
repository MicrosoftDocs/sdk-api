---
UID: NF:wmcontainer.MFCreateASFStreamingMediaSink
title: MFCreateASFStreamingMediaSink function (wmcontainer.h)
description: Creates an activation object for the ASF streaming sink. (MFCreateASFStreamingMediaSink)
helpviewer_keywords: ["MFCreateASFStreamingMediaSink","MFCreateASFStreamingMediaSink function [Media Foundation]","mf.mfcreateasfstreamingmediasink","wmcontainer/MFCreateASFStreamingMediaSink"]
old-location: mf\mfcreateasfstreamingmediasink.htm
tech.root: mf
ms.assetid: bfa34529-e1f9-462b-9c99-b65cd526d364
ms.date: 12/05/2018
ms.keywords: MFCreateASFStreamingMediaSink, MFCreateASFStreamingMediaSink function [Media Foundation], mf.mfcreateasfstreamingmediasink, wmcontainer/MFCreateASFStreamingMediaSink
req.header: wmcontainer.h
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
 - MFCreateASFStreamingMediaSink
 - wmcontainer/MFCreateASFStreamingMediaSink
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
 - MFCreateASFStreamingMediaSink
---

# MFCreateASFStreamingMediaSink function


## -description

Creates an activation object for the ASF streaming sink.

The  ASF streaming sink enables  an application to write streaming Advanced Systems Format (ASF)  packets to an HTTP byte stream.

## -parameters

### -param pIByteStream

 A pointer to a byte stream object in which the ASF media sink writes the streamed content.

### -param ppIMediaSink

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a> interface of the ASF streaming-media sink object. To create the media sink, the application must call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">IMFActivate::ActivateObject</a> on the received pointer. The caller must release the interface pointer.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To create the ASF streaming sink in another process, call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfstreamingmediasinkactivate">MFCreateASFStreamingMediaSinkActivate</a>.
      

An application can get a pointer to the <a href="/windows/desktop/medfound/asf-contentinfo-object">ASF ContentInfo Object</a> by calling <b>IUnknown::QueryInterface</b> on the media sink object received in the <i>ppIMediaSink</i> parameter. The ContentInfo object is used to set the encoder configuration settings, provide stream properties supplied by an ASF profile, and add metadata information. These configuration settings populate the various ASF header objects of the encoded ASF file. For more information, see  
<a href="/windows/desktop/medfound/setting-properties-in-the-contentinfo-object">Setting Properties in the ContentInfo Object</a>.


#### Examples

The following code example shows how to create a media sink for an ASF source. This example copies the stream configuration settings from the source to the ContentInfo object that represents the ASF header object of the output file.


```cpp
//  Creates an an instance of the ASF streaming sink.

HRESULT CreateASFStreamingSink(
    IMFMediaSource *pSource, 
    IMFByteStream  *pOutputByteStream, 
    IMFMediaSink   **ppMediaSink
    )
{
    IMFPresentationDescriptor* pSourcePD = NULL;
    IMFASFProfile* pASFProfile = NULL;;
    IMFMediaSink* pMediaSink = NULL;
    IMFASFContentInfo* pASFContentInfo = NULL;

    // Create the streaming media sink for the ASF file
    HRESULT hr = MFCreateASFStreamingMediaSink(pOutputByteStream, &pMediaSink);
    if (FAILED(hr))
    {
        goto done;
    }

    //
    // Transfer the ASF profile from the media source to the sink.
    //

    // Get the presentation descriptor from the source.
    hr = pSource->CreatePresentationDescriptor(&pSourcePD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Convert the presentation descriptor to an ASF profile.
    hr = MFCreateASFProfileFromPresentationDescriptor(pSourcePD, &pASFProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pMediaSink->QueryInterface(IID_PPV_ARGS(&pASFContentInfo));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the profile on the sink.
    hr = pASFContentInfo->SetProfile(pASFProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppMediaSink = pMediaSink;
    (*ppMediaSink)->AddRef();

done:
    SafeRelease(&pSourcePD);
    SafeRelease(&pASFProfile);
    SafeRelease(&pASFContentInfo);
    SafeRelease(&pMediaSink);
    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfstreamingmediasinkactivate">MFCreateASFStreamingMediaSinkActivate</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
