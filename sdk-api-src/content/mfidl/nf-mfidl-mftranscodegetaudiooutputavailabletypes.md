---
UID: NF:mfidl.MFTranscodeGetAudioOutputAvailableTypes
title: MFTranscodeGetAudioOutputAvailableTypes function
author: windows-sdk-content
description: Gets a list of output formats from an audio encoder.
old-location: mf\mftranscodegetaudiooutputavailabletypes.htm
tech.root: medfound
ms.assetid: 8750eacb-7e6f-4c17-987b-f4baa4eea847
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: MFT_FIELDOFUSE_UNLOCK_Attribute, MFTranscodeGetAudioOutputAvailableTypes, MFTranscodeGetAudioOutputAvailableTypes function [Media Foundation], MF_TRANSCODE_ENCODINGPROFILE, MF_TRANSCODE_QUALITYVSSPEED, mf.mftranscodegetaudiooutputavailabletypes, mfidl/MFTranscodeGetAudioOutputAvailableTypes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFTranscodeGetAudioOutputAvailableTypes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFTranscodeGetAudioOutputAvailableTypes function


## -description


Gets a list of output formats from an audio encoder.


## -parameters




### -param guidSubType [in]

Specifies the subtype of the output media. The encoder uses this value as a filter when it is enumerating the available output types. For information about the audio subtypes, see  <a href="https://msdn.microsoft.com/c38a1194-e2d8-42ca-8581-4054171f6f44">Audio Subtype GUIDs</a>. 


### -param dwMFTFlags [in]

Bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/ba39fb66-d8b6-49c1-8312-18ebdcb012c9">_MFT_ENUM_FLAG</a> enumeration.




### -param pCodecConfig [in]

A pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of an attribute store. The attribute store specifies the encoder configuration settings. This parameter can be <b>NULL</b>. The attribute store can hold any of the following attributes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MFT_FIELDOFUSE_UNLOCK_Attribute"></a><a id="mft_fieldofuse_unlock_attribute"></a><a id="MFT_FIELDOFUSE_UNLOCK_ATTRIBUTE"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/7f48967e-375a-4019-b14f-2f457b616cc0">MFT_FIELDOFUSE_UNLOCK_Attribute</a></b></dt>
</dl>
</td>
<td width="60%">
Set this attribute to unlock an encoder that has field-of-use descriptions.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_TRANSCODE_ENCODINGPROFILE"></a><a id="mf_transcode_encodingprofile"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/9a6b6402-ff53-4399-8616-06b7768a8737">MF_TRANSCODE_ENCODINGPROFILE</a></b></dt>
</dl>
</td>
<td width="60%">
Specifies a device conformance profile for a Windows Media encoder.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_TRANSCODE_QUALITYVSSPEED"></a><a id="mf_transcode_qualityvsspeed"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/872140e8-fd39-446c-a84f-1e04ea95076e">MF_TRANSCODE_QUALITYVSSPEED</a></b></dt>
</dl>
</td>
<td width="60%">
Sets the tradeoff between encoding quality and encoding speed.

</td>
</tr>
</table>
 


### -param ppAvailableTypes [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/fec6aa17-2770-4f53-b36d-b94236093d23">IMFCollection</a> interface of a collection object that contains a list of preferred audio media types. The collection contains <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> pointers. The caller must release the interface pointer.


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

Internally, this function works by calling <a href="https://msdn.microsoft.com/e065ae51-85dd-48ef-9322-de4ade62c0fe">MFTEnumEx</a> to find a matching encoder, and then calling <a href="https://msdn.microsoft.com/d0f75414-18cf-4e76-b875-5f373510c87b">IMFTransform::GetOutputAvailableType</a> to get the encoder's output types.


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




<a href="https://msdn.microsoft.com/a45983a8-4061-40e1-a11a-67de0867e553">IMFCollection::GetElement</a>



<a href="https://msdn.microsoft.com/2a482c6f-6e20-419a-a7eb-085c41cc8186">MFCreateTranscodeProfile</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/2397ca78-edb5-4756-bd07-00529db28f76">Tutorial: Encoding a WMA File</a>
 

 

