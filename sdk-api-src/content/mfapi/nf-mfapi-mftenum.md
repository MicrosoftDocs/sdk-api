---
UID: NF:mfapi.MFTEnum
title: MFTEnum function
author: windows-sdk-content
description: Enumerates Media Foundation transforms (MFTs) in the registry.
old-location: mf\mftenum.htm
tech.root: medfound
ms.assetid: a3bd2b3c-0b0b-4d64-99cc-6093c773f71c
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: MFTEnum, MFTEnum function [Media Foundation], a3bd2b3c-0b0b-4d64-99cc-6093c773f71c, mf.mftenum, mfapi/MFTEnum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFTEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFTEnum function


## -description


Enumerates Media Foundation transforms (MFTs) in the registry.
        

Starting in Windows 7, applications should use the <a href="https://msdn.microsoft.com/e065ae51-85dd-48ef-9322-de4ade62c0fe">MFTEnumEx</a> function instead.


## -parameters




### -param guidCategory [in]

GUID that specifies the category of MFTs to enumerate. For a list of MFT categories, see <a href="https://msdn.microsoft.com/eca3ae3b-e40a-407d-986c-d0a85b891f52">MFT_CATEGORY</a>.
          


### -param Flags [in]

Reserved. Must be zero.
          


### -param pInputType [in]

Pointer to an <a href="https://msdn.microsoft.com/1d26b9ee-545a-4e47-9a68-b9e567f0dec4">MFT_REGISTER_TYPE_INFO</a> structure that specifies an input media type to match. 

This parameter can be <b>NULL</b>. If <b>NULL</b>, all input types are matched.


### -param pOutputType [in]

Pointer to an <a href="https://msdn.microsoft.com/1d26b9ee-545a-4e47-9a68-b9e567f0dec4">MFT_REGISTER_TYPE_INFO</a> structure that specifies an output media type to match.

This parameter can be <b>NULL</b>.
          If <b>NULL</b>, all output types are matched.


### -param pAttributes [in]

Reserved. Set to <b>NULL</b>.

<div class="alert"><b>Note</b>  Windows Vista and Windows Server 2008: This parameter can specify a pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of an attribute store. The <b>MFTEnum</b> function matches the attributes in this object against the attributes stored in the registry. (Registry attributes are specified in the <i>pAttributes</i> parameter of the <a href="https://msdn.microsoft.com/fb3a2b67-d3e4-4d5f-960a-3979f4780904">MFTRegister</a> function.) Only MFTs with matching attributes are returned in the enumeration results.</div>
<div> </div>
<div class="alert"><b>Note</b>  Windows 7 and later: This parameter is ignored.</div>
<div> </div>

### -param ppclsidMFT [out]

Receives a pointer to an array of CLSIDs. To create an MFT from this list, call <b>CoCreateInstance</b> with one of the CLSIDs. To get information about a particular MFT from its CLSID, call <a href="https://msdn.microsoft.com/d1bac1c7-3f9b-46b7-bdf7-c32983c648ee">MFTGetInfo</a>. The caller must free the memory for the array by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.
          


### -param pcMFTs [out]

Receives the number of elements in the <i>ppclsidMFT</i> array. The value can be zero.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function returns a list of all the MFTs in the specified category that match the search criteria given by the <i>pInputType</i>, <i>pOutputType</i>, and <i>pAttributes</i> parameters. Any of those parameters can be <b>NULL</b>.
      

If no MFTs match the criteria, the method succeeds but returns the value zero in <i>pcMFTs</i>.
      


#### Examples

To find a decoder, set <i>guidCategory</i> to <b>MFT_CATEGORY_AUDIO_DECODER</b>or <b>MFT_CATEGORY_VIDEO_DECODER</b>and specify the encoding format in <i>pInputType</i>.  You would typically set <i>pOutputType</i> to <b>NULL</b> in this case.


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


To find an encoder, set <i>guidCategory</i> to <b>MFT_CATEGORY_AUDIO_ENCODER</b>or <b>MFT_CATEGORY_VIDEO_ENCODER</b>and specify the encoding format in <i>pOutputType</i>.  You would typically set <i>pInputType</i> to <b>NULL</b> in this case.


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




<a href="https://msdn.microsoft.com/32c088d5-d9dd-43d3-a63b-219e6a7a36b1">Adding a Decoder to a Topology</a>



<a href="https://msdn.microsoft.com/e065ae51-85dd-48ef-9322-de4ade62c0fe">MFTEnumEx</a>



<a href="https://msdn.microsoft.com/fb3a2b67-d3e4-4d5f-960a-3979f4780904">MFTRegister</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>



<a href="https://msdn.microsoft.com/76d2a703-4162-428e-a4ff-643e346eacfb">Registering and Enumerating MFTs</a>
 

 

