---
UID: NF:mfapi.MFTEnum
title: MFTEnum function (mfapi.h)
description: Enumerates Media Foundation transforms (MFTs) in the registry.
helpviewer_keywords: ["MFTEnum","MFTEnum function [Media Foundation]","a3bd2b3c-0b0b-4d64-99cc-6093c773f71c","mf.mftenum","mfapi/MFTEnum"]
old-location: mf\mftenum.htm
tech.root: mf
ms.assetid: a3bd2b3c-0b0b-4d64-99cc-6093c773f71c
ms.date: 12/05/2018
ms.keywords: MFTEnum, MFTEnum function [Media Foundation], a3bd2b3c-0b0b-4d64-99cc-6093c773f71c, mf.mftenum, mfapi/MFTEnum
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - MFTEnum
 - mfapi/MFTEnum
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
 - MFTEnum
---

# MFTEnum function


## -description

Enumerates Media Foundation transforms (MFTs) in the registry.
        

Starting in Windows 7, applications should use the <a href="/windows/desktop/api/mfapi/nf-mfapi-mftenumex">MFTEnumEx</a> function instead.

## -parameters

### -param guidCategory [in]

GUID that specifies the category of MFTs to enumerate. For a list of MFT categories, see <a href="/windows/desktop/medfound/mft-category">MFT_CATEGORY</a>.

### -param Flags [in]

Reserved. Must be zero.

### -param pInputType [in]

Pointer to an <a href="/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info">MFT_REGISTER_TYPE_INFO</a> structure that specifies an input media type to match. 

This parameter can be <b>NULL</b>. If <b>NULL</b>, all input types are matched.

### -param pOutputType [in]

Pointer to an <a href="/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info">MFT_REGISTER_TYPE_INFO</a> structure that specifies an output media type to match.

This parameter can be <b>NULL</b>.
          If <b>NULL</b>, all output types are matched.

### -param pAttributes [in]

Reserved. Set to <b>NULL</b>.

<div class="alert"><b>Note</b>  Windows Vista and Windows Server 2008: This parameter can specify a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of an attribute store. The <b>MFTEnum</b> function matches the attributes in this object against the attributes stored in the registry. (Registry attributes are specified in the <i>pAttributes</i> parameter of the <a href="/windows/desktop/api/mfapi/nf-mfapi-mftregister">MFTRegister</a> function.) Only MFTs with matching attributes are returned in the enumeration results.</div>
<div> </div>
<div class="alert"><b>Note</b>  Windows 7 and later: This parameter is ignored.</div>
<div> </div>

### -param ppclsidMFT [out]

Receives a pointer to an array of CLSIDs. To create an MFT from this list, call <b>CoCreateInstance</b> with one of the CLSIDs. To get information about a particular MFT from its CLSID, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mftgetinfo">MFTGetInfo</a>. The caller must free the memory for the array by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -param pcMFTs [out]

Receives the number of elements in the <i>ppclsidMFT</i> array. The value can be zero.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function returns a list of all the MFTs in the specified category that match the search criteria given by the <i>pInputType</i>, <i>pOutputType</i>, and <i>pAttributes</i> parameters. Any of those parameters can be <b>NULL</b>.
      

If no MFTs match the criteria, the method succeeds but returns the value zero in <i>pcMFTs</i>.
      


#### Examples

To find a decoder, set <i>guidCategory</i> to <b>MFT_CATEGORY_AUDIO_DECODER</b> or <b>MFT_CATEGORY_VIDEO_DECODER</b> and specify the encoding format in <i>pInputType</i>.  You would typically set <i>pOutputType</i> to <b>NULL</b> in this case.


```cpp
HRESULT FindDecoder(
    const GUID& subtype,        // Subtype
    BOOL bAudio,                // TRUE for audio, FALSE for video
    IMFTransform **ppDecoder    // Receives a pointer to the decoder.
    )
{
    HRESULT hr = S_OK;
    UINT32 count = 0;

    CLSID *ppCLSIDs = NULL;

    MFT_REGISTER_TYPE_INFO info = { 0 };

    info.guidMajorType = bAudio ? MFMediaType_Audio : MFMediaType_Video;
    info.guidSubtype = subtype;

    hr = MFTEnum(   
        bAudio ? MFT_CATEGORY_AUDIO_DECODER : MFT_CATEGORY_VIDEO_DECODER,
        0,      // Reserved
        &info,  // Input type
        NULL,   // Output type
        NULL,   // Reserved
        &ppCLSIDs,
        &count
        );

    if (SUCCEEDED(hr) && count == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
    }

    // Create the first decoder in the list.

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(ppCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(ppDecoder));
    }

    CoTaskMemFree(ppCLSIDs);
    return hr;
}

```


To find an encoder, set <i>guidCategory</i> to <b>MFT_CATEGORY_AUDIO_ENCODER</b> or <b>MFT_CATEGORY_VIDEO_ENCODER</b> and specify the encoding format in <i>pOutputType</i>.  You would typically set <i>pInputType</i> to <b>NULL</b> in this case.


```cpp
HRESULT FindEncoder(
    const GUID& subtype, 
    BOOL bAudio, 
    IMFTransform **ppEncoder
    )
{
    HRESULT hr = S_OK;
    UINT32 count = 0;

    CLSID *ppCLSIDs = NULL;

    MFT_REGISTER_TYPE_INFO info = { 0 };

    info.guidMajorType = bAudio ? MFMediaType_Audio : MFMediaType_Video;
    info.guidSubtype = subtype;

    hr = MFTEnum(   
        bAudio ? MFT_CATEGORY_AUDIO_ENCODER : MFT_CATEGORY_VIDEO_ENCODER,
        0,          // Reserved
        NULL,       // Input type
        &info,      // Output type
        NULL,       // Reserved
        &ppCLSIDs,
        &count
        );

    if (SUCCEEDED(hr) && count == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
    }

    // Create the first encoder in the list.

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(ppCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(ppEncoder));
    }

    CoTaskMemFree(ppCLSIDs);
    return hr;
}

```

## -see-also

<a href="/windows/desktop/medfound/adding-a-decoder-to-a-topology">Adding a Decoder to a Topology</a>



<a href="/windows/desktop/api/mfapi/nf-mfapi-mftenumex">MFTEnumEx</a>



<a href="/windows/desktop/api/mfapi/nf-mfapi-mftregister">MFTRegister</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>



<a href="/windows/desktop/medfound/registering-and-enumerating-mfts">Registering and Enumerating MFTs</a>