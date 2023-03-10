---
UID: NF:mfidl.MFTranscodeGetAudioOutputAvailableTypes
title: MFTranscodeGetAudioOutputAvailableTypes function (mfidl.h)
description: Gets a list of output formats from an audio encoder.
helpviewer_keywords: ["MFT_FIELDOFUSE_UNLOCK_Attribute","MFTranscodeGetAudioOutputAvailableTypes","MFTranscodeGetAudioOutputAvailableTypes function [Media Foundation]","MF_TRANSCODE_ENCODINGPROFILE","MF_TRANSCODE_QUALITYVSSPEED","mf.mftranscodegetaudiooutputavailabletypes","mfidl/MFTranscodeGetAudioOutputAvailableTypes"]
old-location: mf\mftranscodegetaudiooutputavailabletypes.htm
tech.root: mf
ms.assetid: 8750eacb-7e6f-4c17-987b-f4baa4eea847
ms.date: 12/05/2018
ms.keywords: MFT_FIELDOFUSE_UNLOCK_Attribute, MFTranscodeGetAudioOutputAvailableTypes, MFTranscodeGetAudioOutputAvailableTypes function [Media Foundation], MF_TRANSCODE_ENCODINGPROFILE, MF_TRANSCODE_QUALITYVSSPEED, mf.mftranscodegetaudiooutputavailabletypes, mfidl/MFTranscodeGetAudioOutputAvailableTypes
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
 - MFTranscodeGetAudioOutputAvailableTypes
 - mfidl/MFTranscodeGetAudioOutputAvailableTypes
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
 - MFTranscodeGetAudioOutputAvailableTypes
---

# MFTranscodeGetAudioOutputAvailableTypes function


## -description

Gets a list of output formats from an audio encoder.

## -parameters

### -param guidSubType [in]

Specifies the subtype of the output media. The encoder uses this value as a filter when it is enumerating the available output types. For information about the audio subtypes, see  <a href="/windows/desktop/medfound/audio-subtype-guids">Audio Subtype GUIDs</a>.

### -param dwMFTFlags [in]

Bitwise <b>OR</b> of zero or more flags from the <a href="/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag">_MFT_ENUM_FLAG</a> enumeration.

### -param pCodecConfig [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of an attribute store. The attribute store specifies the encoder configuration settings. This parameter can be <b>NULL</b>. The attribute store can hold any of the following attributes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MFT_FIELDOFUSE_UNLOCK_Attribute"></a><a id="mft_fieldofuse_unlock_attribute"></a><a id="MFT_FIELDOFUSE_UNLOCK_ATTRIBUTE"></a><dl>
<dt><b><a href="/windows/desktop/medfound/mft-fieldofuse-unlock-attribute">MFT_FIELDOFUSE_UNLOCK_Attribute</a></b></dt>
</dl>
</td>
<td width="60%">
Set this attribute to unlock an encoder that has field-of-use descriptions.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_TRANSCODE_ENCODINGPROFILE"></a><a id="mf_transcode_encodingprofile"></a><dl>
<dt><b><a href="/windows/desktop/medfound/mf-transcode-encodingprofile">MF_TRANSCODE_ENCODINGPROFILE</a></b></dt>
</dl>
</td>
<td width="60%">
Specifies a device conformance profile for a Windows Media encoder.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_TRANSCODE_QUALITYVSSPEED"></a><a id="mf_transcode_qualityvsspeed"></a><dl>
<dt><b><a href="/windows/desktop/medfound/mf-transcode-qualityvsspeed">MF_TRANSCODE_QUALITYVSSPEED</a></b></dt>
</dl>
</td>
<td width="60%">
Sets the tradeoff between encoding quality and encoding speed.

</td>
</tr>
</table>

### -param ppAvailableTypes [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection">IMFCollection</a> interface of a collection object that contains a list of preferred audio media types. The collection contains <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> pointers. The caller must release the interface pointer.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function call succeeded. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSCODE_NO_MATCHING_ENCODER</b></dt>
</dl>
</td>
<td width="60%">
Failed to find an encoder that matches the specified configuration settings.

</td>
</tr>
</table>

## -remarks

This function assumes the encoder will be used in its default encoding mode, which is typically constant bit-rate (CBR) encoding. Therefore, the types returned by the function might not work with other modes, such as variable bit-rate (VBR) encoding.

Internally, this function works by calling <a href="/windows/desktop/api/mfapi/nf-mfapi-mftenumex">MFTEnumEx</a> to find a matching encoder, and then calling <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype">IMFTransform::GetOutputAvailableType</a> to get the encoder's output types.


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

<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement">IMFCollection::GetElement</a>



<a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile">MFCreateTranscodeProfile</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/tutorial--converting-an-mp3-file-to-a-wma-file">Tutorial: Encoding a WMA File</a>