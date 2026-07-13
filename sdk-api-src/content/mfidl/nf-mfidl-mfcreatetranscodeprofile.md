---
UID: NF:mfidl.MFCreateTranscodeProfile
title: MFCreateTranscodeProfile function (mfidl.h)
description: Creates an empty transcode profile object.
helpviewer_keywords: ["MFCreateTranscodeProfile","MFCreateTranscodeProfile function [Media Foundation]","mf.mfcreatetranscodeprofile","mfidl/MFCreateTranscodeProfile"]
old-location: mf\mfcreatetranscodeprofile.htm
tech.root: mf
ms.assetid: 2a482c6f-6e20-419a-a7eb-085c41cc8186
ms.date: 12/05/2018
ms.keywords: MFCreateTranscodeProfile, MFCreateTranscodeProfile function [Media Foundation], mf.mfcreatetranscodeprofile, mfidl/MFCreateTranscodeProfile
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
 - MFCreateTranscodeProfile
 - mfidl/MFCreateTranscodeProfile
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
 - MFCreateTranscodeProfile
---

# MFCreateTranscodeProfile function


## -description

Creates an empty transcode profile object.

The transcode profile stores configuration settings for the output file. These configuration settings are specified by the caller, and include audio and video stream properties, encoder settings, and  container settings. To set these properties, the caller must call the appropriate <a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile">IMFTranscodeProfile</a> methods.

The configured transcode profile is passed to the <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology">MFCreateTranscodeTopology</a> function.  The underlying topology builder uses these settings to build the transcode topology.

## -parameters

### -param ppTranscodeProfile [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile">IMFTranscodeProfile</a> interface of the transcode profile object. Caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>MFCreateTranscodeProfile</b> function creates an empty transcode profile. You must configure the transcode profile setting attributes that define the media types and the container properties. Use the following methods to configure the profile:

<ul>
<li>
<a href="/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes">IMFTranscodeProfile::SetAudioAttributes</a>
</li>
<li>
<a href="/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes">IMFTranscodeProfile::SetVideoAttributes</a>
</li>
<li>
<a href="/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes">IMFTranscodeProfile::SetContainerAttributes</a>
</li>
</ul>
For example code that uses this function, see the following topics:

<ul>
<li>
<a href="/windows/desktop/medfound/tutorial--encoding-an-mp4-file-">Tutorial: Encoding an MP4 File</a>
</li>
<li>
<a href="/windows/desktop/medfound/tutorial--converting-an-mp3-file-to-a-wma-file">Tutorial: Encoding a WMA File</a>
</li>
</ul>

#### Examples

The following example creates a transcode profile for Windows Media Audio (WMA).


```cpp
template <class Q>
HRESULT GetCollectionObject(IMFCollection *pCollection, DWORD index, Q **ppObj)
{
    IUnknown *pUnk;
    HRESULT hr = pCollection->GetElement(index, &pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_PPV_ARGS(ppObj));
        pUnk->Release();
    }
    return hr;
}

HRESULT CreateTranscodeProfile(IMFTranscodeProfile **ppProfile)
{
    IMFTranscodeProfile *pProfile = NULL;     // Transcode profile.
    IMFCollection   *pAvailableTypes = NULL;  // List of audio media types.
    IMFMediaType    *pAudioType = NULL;       // Audio media type.
    IMFAttributes   *pAudioAttrs = NULL;      // Copy of the audio media type.
    IMFAttributes   *pContainer = NULL;       // Container attributes.

    DWORD dwMTCount = 0;
    
    // Create an empty transcode profile.
    HRESULT hr = MFCreateTranscodeProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get output media types for the Windows Media audio encoder.

    // Enumerate all codecs except for codecs with field-of-use restrictions.
    // Sort the results.

    DWORD dwFlags = 
        (MFT_ENUM_FLAG_ALL & (~MFT_ENUM_FLAG_FIELDOFUSE)) | 
        MFT_ENUM_FLAG_SORTANDFILTER;

    hr = MFTranscodeGetAudioOutputAvailableTypes(MFAudioFormat_WMAudioV9, 
        dwFlags, NULL, &pAvailableTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAvailableTypes->GetElementCount(&dwMTCount);
    if (FAILED(hr))
    {
        goto done;
    }
    if (dwMTCount == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Get the first audio type in the collection and make a copy.
    hr = GetCollectionObject(pAvailableTypes, 0, &pAudioType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateAttributes(&pAudioAttrs, 0);       
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioType->CopyAllItems(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the audio attributes on the profile.
    hr = pProfile->SetAudioAttributes(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the container attributes.
    hr = MFCreateAttributes(&pContainer, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pContainer->SetGUID(MF_TRANSCODE_CONTAINERTYPE, MFTranscodeContainerType_ASF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->SetContainerAttributes(pContainer);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppProfile = pProfile;
    (*ppProfile)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pAvailableTypes);
    SafeRelease(&pAudioType);
    SafeRelease(&pAudioAttrs);
    SafeRelease(&pContainer);
    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile">IMFTranscodeProfile</a>



<a href="/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes">MFTranscodeGetAudioOutputAvailableTypes</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/transcode-api">Transcode API</a>