---
UID: NN:mfidl.IMFTranscodeSinkInfoProvider
title: IMFTranscodeSinkInfoProvider (mfidl.h)
description: Implemented by the transcode sink activation object.helpviewer_keywords: ["IMFTranscodeSinkInfoProvider","IMFTranscodeSinkInfoProvider interface [Media Foundation]","IMFTranscodeSinkInfoProvider interface [Media Foundation]","described","mf.imftranscodesinkinfoprovider","mfidl/IMFTranscodeSinkInfoProvider"]
old-location: mf\imftranscodesinkinfoprovider.htm
tech.root: medfound
ms.assetid: c5eb0c30-559a-44dd-80d4-4b11933dc7ce
ms.date: 12/05/2018
ms.keywords: IMFTranscodeSinkInfoProvider, IMFTranscodeSinkInfoProvider interface [Media Foundation], IMFTranscodeSinkInfoProvider interface [Media Foundation],described, mf.imftranscodesinkinfoprovider, mfidl/IMFTranscodeSinkInfoProvider
f1_keywords:
- mfidl/IMFTranscodeSinkInfoProvider
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfidl.h
api_name:
- IMFTranscodeSinkInfoProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTranscodeSinkInfoProvider interface


## -description


Implemented by the transcode sink activation object.

The transcode sink activation object can be used to create any of the following file sinks:
<ul>
<li>3GP file sink</li>
<li>MP3 file sink</li>
<li>MP4 file sink</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTranscodeSinkInfoProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTranscodeSinkInfoProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTranscodeSinkInfoProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftranscodesinkinfoprovider-getsinkinfo">GetSinkInfo</a>
</td>
<td align="left" width="63%">
Gets the audio stream and the video stream attributes specified in the transcode profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftranscodesinkinfoprovider-setoutputbytestream">SetOutputByteStream</a>
</td>
<td align="left" width="63%">
Sets the output byte stream for the transcode media sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftranscodesinkinfoprovider-setoutputfile">SetOutputFile</a>
</td>
<td align="left" width="63%">
Sets the name of the output file to which the media sink writes the transcoded content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftranscodesinkinfoprovider-setprofile">SetProfile</a>
</td>
<td align="left" width="63%">
Sets the specified transcode profile that contains the configuration settings for the audio stream, the video stream, and the container to which the file is written.

</td>
</tr>
</table> 


## -remarks



To use this interface, perform the following steps:

<ol>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodesinkactivate">MFCreateTranscodeSinkActivate</a> to create the transcode sink activation object.</li>
<li>Query the activation object for the <b>IMFTranscodeSinkInfoProvider</b> interface.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile">MFCreateTranscodeProfile</a> to create a transcode profile.</li>
<li>Set the <a href="https://docs.microsoft.com/windows/desktop/medfound/mf-transcode-containertype">MF_TRANSCODE_CONTAINERTYPE</a> attribute on the transcode profile. The attribute must have one of the following values:<ul>
<li><b>MFTranscodeContainerType_3GP</b></li>
<li><b>MFTranscodeContainerType_MP3</b></li>
<li><b>MFTranscodeContainerType_MPEG4</b></li>
</ul>
</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes">IMFTranscodeProfile::SetVideoAttributes</a> and <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes">IMFTranscodeProfile::SetAudioAttributes</a> to specify the video and audio formats.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftranscodesinkinfoprovider-setprofile">IMFTranscodeSinkInfoProvider::SetProfile</a> to set the transcode profile.</li>
<li>Call one of the following methods (but not both) to specify the output file:<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftranscodesinkinfoprovider-setoutputbytestream">IMFTranscodeSinkInfoProvider::SetOutputByteStream</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftranscodesinkinfoprovider-setoutputfile">IMFTranscodeSinkInfoProvider::SetOutputFile</a>
</li>
</ul>
</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">IMFActivate::ActivateObject</a> on the activation object to create the media sink.</li>
</ol>

#### Examples


```cpp
// Creates an activation object for the generic transcode sink.

HRESULT CreateTranscodeSinkActivate(
    REFGUID         guidContainerType,
    IMFAttributes   *pVideoAttributes,
    IMFAttributes   *pAudioAttributes,
    IMFActivate     *pByteStreamActivate, 
    IMFActivate     **ppSinkActivate
    )
{
    IMFActivate* pSinkActivate = NULL;
    IMFTranscodeSinkInfoProvider* pSinkInfoProvider = NULL;
    IMFTranscodeProfile* pProfile = NULL;
    IMFAttributes* pContainerAttributes = NULL;

    HRESULT hr = MFCreateAttributes(&pContainerAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the transcode profile.
    hr = MFCreateTranscodeProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the profile attributes.

    hr = pContainerAttributes->SetGUID(MF_TRANSCODE_CONTAINERTYPE, guidContainerType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->SetContainerAttributes(pContainerAttributes);
    if (FAILED(hr))
    {
        goto done;
    }

    if (pVideoAttributes)
    {
        hr = pProfile->SetVideoAttributes(pVideoAttributes);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    if (pAudioAttributes)
    {
        hr = pProfile->SetAudioAttributes(pAudioAttributes);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Create the transcode sink activation object.
    hr = MFCreateTranscodeSinkActivate(&pSinkActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSinkActivate->QueryInterface(IID_PPV_ARGS(&pSinkInfoProvider));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the output byte stream.
    hr = pSinkInfoProvider->SetOutputByteStream(pByteStreamActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the transcode profile.
    hr = pSinkInfoProvider->SetProfile(pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the activation object to the caller.
    *ppSinkActivate = pSinkActivate;
    (*ppSinkActivate)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pSinkInfoProvider);
    SafeRelease(&pSinkActivate);
    SafeRelease(&pContainerAttributes);
    return hr;
}

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodesinkactivate">MFCreateTranscodeSinkActivate</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

