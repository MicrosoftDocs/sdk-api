---
UID: NF:mfapi.MFTEnumEx
title: MFTEnumEx function (mfapi.h)
description: Gets a list of Microsoft Media Foundation transforms (MFTs) that match specified search criteria. This function extends the MFTEnum function.
helpviewer_keywords: ["MFTEnumEx","MFTEnumEx function [Media Foundation]","mf.mftenumex","mfapi/MFTEnumEx"]
old-location: mf\mftenumex.htm
tech.root: mf
ms.assetid: e065ae51-85dd-48ef-9322-de4ade62c0fe
ms.date: 12/05/2018
ms.keywords: MFTEnumEx, MFTEnumEx function [Media Foundation], mf.mftenumex, mfapi/MFTEnumEx
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFTEnumEx
 - mfapi/MFTEnumEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFTEnumEx
---

# MFTEnumEx function


## -description

Gets a list of Microsoft Media Foundation transforms (MFTs) that match specified search criteria. This function extends the <a href="/windows/desktop/api/mfapi/nf-mfapi-mftenum">MFTEnum</a> function.

## -parameters

### -param guidCategory [in]

A GUID that specifies the category of MFTs to enumerate. For a list of MFT categories, see <a href="/windows/desktop/medfound/mft-category">MFT_CATEGORY</a>.

### -param Flags [in]

The bitwise <b>OR</b> of zero or more flags from the <a href="/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag">_MFT_ENUM_FLAG</a> enumeration.

### -param pInputType [in]

A pointer to an <a href="/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info">MFT_REGISTER_TYPE_INFO</a> structure that specifies an input media type to match. 

This parameter can be <b>NULL</b>. If <b>NULL</b>, all input types are matched.

### -param pOutputType [in]

A pointer to an <a href="/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info">MFT_REGISTER_TYPE_INFO</a> structure that specifies an output media type to match.

This parameter can be <b>NULL</b>. If <b>NULL</b>, all output types are matched.

### -param pppMFTActivate [out]

Receives an array of <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface pointers. Each pointer represents an activation object for an MFT that matches the search criteria. The function allocates the memory for the array. The caller must release the pointers and call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory for the array.

### -param pnumMFTActivate [out]

Receives the number of elements in the <i>pppMFTActivate</i> array. If no MFTs match the search criteria, this parameter receives the value zero.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <i>Flags</i> parameter controls which MFTs are enumerated, and the order in which they are returned. The flags for this parameter fall into several groups.


The first set of flags specifies how an MFT processes data.



<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="MFT_ENUM_FLAG_SYNCMFT"></a><a id="mft_enum_flag_syncmft"></a>MFT_ENUM_FLAG_SYNCMFT

</td>
<td width="60%">
The MFT performs synchronous data processing in software. This is the original MFT processing model, and is  compatible with Windows Vista.

</td>
</tr>
<tr>
<td width="40%">
<a id="MFT_ENUM_FLAG_ASYNCMFT"></a><a id="mft_enum_flag_asyncmft"></a>MFT_ENUM_FLAG_ASYNCMFT

</td>
<td width="60%">
The MFT performs asynchronous data processing in software. This processing model requires Windows 7. For more information, see <a href="/windows/desktop/medfound/asynchronous-mfts">Asynchronous MFTs</a>.

</td>
</tr>
<tr>
<td width="40%">
<a id="MFT_ENUM_FLAG_HARDWARE"></a><a id="mft_enum_flag_hardware"></a>MFT_ENUM_FLAG_HARDWARE

</td>
<td width="60%">
The MFT performs hardware-based data processing, using either the AVStream driver or a GPU-based proxy MFT. MFTs in this category always process data asynchronously. For more information, see <a href="/windows/desktop/medfound/hardware-mfts">Hardware MFTs</a>.

</td>
</tr>
</table>
 

Every MFT falls into exactly one of these categories.  To enumerate a category, set the corresponding flag in the <i>Flags</i> parameter. You can combine these flags to enumerate more than one category. If none of these flags is specified, the default category is synchronous MFTs (<b>MFT_ENUM_FLAG_SYNCMFT</b>).



Next, the following flags include MFTs that are otherwise  excluded from the results. By default, flags that match these criteria are excluded from the results. Use any these flags to include them.



<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="MFT_ENUM_FLAG_FIELDOFUSE"></a><a id="mft_enum_flag_fieldofuse"></a><b>MFT_ENUM_FLAG_FIELDOFUSE</b>

</td>
<td width="60%">
Include MFTs that must be unlocked by the application.

</td>
</tr>
<tr>
<td width="40%">
<a id="MFT_ENUM_FLAG_LOCALMFT"></a><a id="mft_enum_flag_localmft"></a><b>MFT_ENUM_FLAG_LOCALMFT</b>

</td>
<td width="60%">
Include MFTs that are registered in the caller's process through either the <a href="/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal">MFTRegisterLocal</a> or <a href="/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid">MFTRegisterLocalByCLSID</a> function.

</td>
</tr>
<tr>
<td width="40%">
<a id="MFT_ENUM_FLAG_TRANSCODE_ONLY"></a><a id="mft_enum_flag_transcode_only"></a><b>MFT_ENUM_FLAG_TRANSCODE_ONLY</b>

</td>
<td width="60%">
Include MFTs that are optimized for transcoding rather than playback.

</td>
</tr>
</table>
 





The last flag is used to sort and filter the results:



<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="MFT_ENUM_FLAG_SORTANDFILTER"></a><a id="mft_enum_flag_sortandfilter"></a><b>MFT_ENUM_FLAG_SORTANDFILTER</b>

</td>
<td width="60%">
Sort and filter the results.

</td>
</tr>
</table>
 



If the <b>MFT_ENUM_FLAG_SORTANDFILTER</b> flag is set, the <b>MFTEnumEx</b> function sorts the results as follows:

<ul>
<li>Local: If the <b>MFT_ENUM_FLAG_LOCALMFT</b> flag is set, local MFTs appear first in the list. To register a local MFT, call the <a href="/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal">MFTRegisterLocal</a> or <a href="/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid">MFTRegisterLocalByCLSID</a> function.</li>
<li>Merit: MFTs with a merit value appear next on the list, in order of merit value (highest to lowest). For more information about merit, see <a href="/windows/desktop/medfound/mft-codec-merit-attribute">MFT_CODEC_MERIT_Attribute</a>. </li>
<li>Preferred: If an MFT is listed in the plug-in control's preferred list, it appears next in the list. For more information about the plug-in control, see <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol">IMFPluginControl</a>.</li>
<li>If an MFT appears on the blocked list, it is excluded from the results. For more information about the blocked list, see <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfplugincontrol-isdisabled">IMFPluginControl::IsDisabled</a>.</li>
<li>Any other MFTs that match the search criteria appear at the end of the list, unsorted.</li>
</ul>
If you do not set the <b>MFT_ENUM_FLAG_SORTANDFILTER</b> flag, the <b>MFTEnumEx</b> function returns an unsorted list.

Setting the <i>Flags</i> parameter to zero is equivalent to using the value <b>MFT_ENUM_FLAG_SYNCMFT</b> | <b>MFT_ENUM_FLAG_LOCALMFT</b> | <b>MFT_ENUM_FLAG_SORTANDFILTER</b>.

Setting <i>Flags</i> to <b>MFT_ENUM_FLAG_SYNCMFT</b> is equivalent to calling the <a href="/windows/desktop/api/mfapi/nf-mfapi-mftenum">MFTEnum</a> function.

If no MFTs match the search criteria, the function returns <b>S_OK</b>, unless some other error occurs. Therefore, always check the count received in the <i>pcMFTActivate</i> parameter before you dereference the <i>pppMFTActivate</i> pointer.

<div class="alert"><b>Note</b>  There is no way to enumerate just local MFTs and nothing else. Setting <i>Flags</i> equal to <b>MFT_ENUM_FLAG_LOCALMFT</b> is equivalent to  including the <b>MFT_ENUM_FLAG_SYNCMFT</b> flag. However, if you also sort the results by specifying the <b>MFT_ENUM_FLAG_SORTANDFILTER</b> flag, local MFTs appear first in the list.</div>
<div> </div>
<h3><a id="Creating_the_MFT"></a><a id="creating_the_mft"></a><a id="CREATING_THE_MFT"></a>Creating the MFT</h3>
If at least one MFT matches the search criteria, the <i>pppMFTActivate</i> parameter receives an array of <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> pointers. One pointer is returned for each matching MFT. Each pointer represents an <i>activation object</i> for the MFT. For more information, see <a href="/windows/desktop/medfound/activation-objects">Activation Objects</a>.

Additional information about each MFT is stored as attributes on the activation objects. For a list of the possible attributes, see <a href="/windows/desktop/medfound/transform-attributes">Transform Attributes</a>.

To create an instance of the MFT, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">IMFActivate::ActivateObject</a>.

<h3><a id="Hardware_Codecs"></a><a id="hardware_codecs"></a><a id="HARDWARE_CODECS"></a>Hardware Codecs</h3>
Hardware codecs are excluded from the enumeration results if the following registry keys are set to zero:

Decoders: <b>HKEY_LOCAL_MACHINE</b>&#92;<b>SOFTWARE</b>&#92;<b>Microsoft</b>&#92;<b>Windows Media Foundation</b>&#92;<b>HardwareMFT</b>&#92;<b>EnableDecoders</b>



Encoders: <b>HKEY_LOCAL_MACHINE</b>&#92;<b>SOFTWARE</b>&#92;<b>Microsoft</b>&#92;<b>Windows Media Foundation</b>&#92;<b>HardwareMFT</b>&#92;<b>EnableEncoders</b>



Video processors: <b>HKEY_LOCAL_MACHINE</b>&#92;<b>SOFTWARE</b>&#92;<b>Microsoft</b>&#92;<b>Windows Media Foundation</b>&#92;<b>HardwareMFT</b>&#92;<b>EnableVideoProcessors</b>



These keys are intended for OEMs, and should not be used by applications.

For hardware codecs, the <i>guidCategory</i> parameter of <b>MFTEnumEx</b> can also specify one of the following kernel streaming (KS) device categories:

<ul>
<li><b>KSCATEGORY_DATACOMPRESSOR</b></li>
<li><b>KSCATEGORY_DATADECOMPRESSOR</b></li>
</ul>
Hardware codecs should also be registered under an <a href="/windows/desktop/medfound/mft-category">MFT_CATEGORY</a> GUID, so applications should generally use those categories instead of the KS device categories.


#### Examples

The following example searches for a video or audio decoder. Asynchronous, hardware, transcode, and field-of-use decoders are excluded. If a match is found, the code creates the first MFT in the list.


```cpp
HRESULT FindDecoderEx(
    const GUID& subtype,        // Subtype
    BOOL bAudio,                // TRUE for audio, FALSE for video
    IMFTransform **ppDecoder    // Receives a pointer to the decoder.
    )
{
    HRESULT hr = S_OK;
    UINT32 count = 0;

    IMFActivate **ppActivate = NULL;

    MFT_REGISTER_TYPE_INFO info = { 0 };

    info.guidMajorType = bAudio ? MFMediaType_Audio : MFMediaType_Video;
    info.guidSubtype = subtype;

    hr = MFTEnumEx(
        bAudio ? MFT_CATEGORY_AUDIO_DECODER : MFT_CATEGORY_VIDEO_DECODER,
        MFT_ENUM_FLAG_SYNCMFT | MFT_ENUM_FLAG_LOCALMFT | MFT_ENUM_FLAG_SORTANDFILTER,
        &info,      // Input type
        NULL,       // Output type
        &ppActivate,
        &count
        );

    if (SUCCEEDED(hr) && count == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
    }

    // Create the first decoder in the list.

    if (SUCCEEDED(hr))
    {
        hr = ppActivate[0]->ActivateObject(IID_PPV_ARGS(ppDecoder));
    }

    for (UINT32 i = 0; i < count; i++)
    {
        ppActivate[i]->Release();
    }
    CoTaskMemFree(ppActivate);

    return hr;
}

```


The next example searches for a video or audio encoder. Asynchronous, hardware, transcode, and field-of-use encoders are excluded.


```cpp
HRESULT FindEncoderEx(
    const GUID& subtype,        // Subtype
    BOOL bAudio,                // TRUE for audio, FALSE for video
    IMFTransform **ppEncoder    // Receives a pointer to the decoder.
    )
{
    HRESULT hr = S_OK;
    UINT32 count = 0;

    IMFActivate **ppActivate = NULL;

    MFT_REGISTER_TYPE_INFO info = { 0 };

    info.guidMajorType = bAudio ? MFMediaType_Audio : MFMediaType_Video;
    info.guidSubtype = subtype;

    hr = MFTEnumEx(
        bAudio ? MFT_CATEGORY_AUDIO_ENCODER : MFT_CATEGORY_VIDEO_ENCODER,
        MFT_ENUM_FLAG_SYNCMFT | MFT_ENUM_FLAG_LOCALMFT | MFT_ENUM_FLAG_SORTANDFILTER,
        NULL,       // Input type
        &info,      // Output type
        &ppActivate,
        &count
        );

    if (SUCCEEDED(hr) && count == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
    }

    // Create the first encoder in the list.

    if (SUCCEEDED(hr))
    {
        hr = ppActivate[0]->ActivateObject(IID_PPV_ARGS(ppEncoder));
    }

    for (UINT32 i = 0; i < count; i++)
    {
        ppActivate[i]->Release();
    }
    CoTaskMemFree(ppActivate);

    return hr;
}

```


The next example searches for a video decoder, with options to include asynchronous, hardware, or transcode decoders.


```cpp
HRESULT FindVideoDecoder(
    const GUID& subtype,
    BOOL bAllowAsync,
    BOOL bAllowHardware, 
    BOOL bAllowTranscode,
    IMFTransform **ppDecoder
    )
{
    HRESULT hr = S_OK;
    UINT32 count = 0;

    IMFActivate **ppActivate = NULL;

    MFT_REGISTER_TYPE_INFO info = { MFMediaType_Video, subtype };

    UINT32 unFlags = MFT_ENUM_FLAG_SYNCMFT  | MFT_ENUM_FLAG_LOCALMFT | 
                     MFT_ENUM_FLAG_SORTANDFILTER;

    if (bAllowAsync)
    {
        unFlags |= MFT_ENUM_FLAG_ASYNCMFT;
    }
    if (bAllowHardware)
    {
        unFlags |= MFT_ENUM_FLAG_HARDWARE;
    }
    if (bAllowTranscode)
    {
        unFlags |= MFT_ENUM_FLAG_TRANSCODE_ONLY;
    }

    hr = MFTEnumEx(MFT_CATEGORY_VIDEO_DECODER,
        unFlags,
        &info,      // Input type
        NULL,       // Output type
        &ppActivate,
        &count);
  
    if (SUCCEEDED(hr) && count == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
    }

    // Create the first decoder in the list.
    if (SUCCEEDED(hr))
    {
        hr = ppActivate[0]->ActivateObject(IID_PPV_ARGS(ppDecoder));
    }

    for (UINT32 i = 0; i < count; i++)
    {
        ppActivate[i]->Release();
    }
    CoTaskMemFree(ppActivate);

    return hr;
}

```


<div class="code"></div>

## -see-also

<a href="/windows/desktop/medfound/field-of-use-restrictions">Field of Use Restrictions</a>



<a href="/windows/desktop/api/mfapi/nf-mfapi-mftregister">MFTRegister</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/registering-and-enumerating-mfts">Registering and Enumerating MFTs</a>