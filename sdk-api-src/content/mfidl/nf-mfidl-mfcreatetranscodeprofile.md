---
UID: NF:mfidl.MFCreateTranscodeProfile
title: MFCreateTranscodeProfile function
author: windows-sdk-content
description: Creates an empty transcode profile object.
old-location: mf\mfcreatetranscodeprofile.htm
tech.root: medfound
ms.assetid: 2a482c6f-6e20-419a-a7eb-085c41cc8186
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: MFCreateTranscodeProfile, MFCreateTranscodeProfile function [Media Foundation], mf.mfcreatetranscodeprofile, mfidl/MFCreateTranscodeProfile
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
 - MFCreateTranscodeProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateTranscodeProfile function


## -description


Creates an empty transcode profile object.

The transcode profile stores configuration settings for the output file. These configuration settings are specified by the caller, and include audio and video stream properties, encoder settings, and  container settings. To set these properties, the caller must call the appropriate <a href="https://msdn.microsoft.com/82e012e0-84d8-4791-8b6f-bda58b498a90">IMFTranscodeProfile</a> methods.

The configured transcode profile is passed to the <a href="https://msdn.microsoft.com/ef3f19bf-1db9-459d-9617-d6cca9d6aba7">MFCreateTranscodeTopology</a> function.  The underlying topology builder uses these settings to build the transcode topology.


## -parameters




### -param ppTranscodeProfile [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/82e012e0-84d8-4791-8b6f-bda58b498a90">IMFTranscodeProfile</a> interface of the transcode profile object. Caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>MFCreateTranscodeProfile</b> function creates an empty transcode profile. You must configure the transcode profile setting attributes that define the media types and the container properties. Use the following methods to configure the profile:

<ul>
<li>
<a href="https://msdn.microsoft.com/4118bb2b-8373-434a-896b-de5a1ba8c793">IMFTranscodeProfile::SetAudioAttributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e68653c5-5663-4839-a482-2244e147f4b9">IMFTranscodeProfile::SetVideoAttributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c62021cf-85f1-4a85-9263-b7883464f5f8">IMFTranscodeProfile::SetContainerAttributes</a>
</li>
</ul>
For example code that uses this function, see the following topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/60873aa6-46ec-4a73-94b9-0d8ac602f850">Tutorial: Encoding an MP4 File</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2397ca78-edb5-4756-bd07-00529db28f76">Tutorial: Encoding a WMA File</a>
</li>
</ul>

#### Examples

The following example creates a transcode profile for Windows Media Audio (WMA).

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>template &lt;class Q&gt;
HRESULT GetCollectionObject(IMFCollection *pCollection, DWORD index, Q **ppObj)
{
    IUnknown *pUnk;
    HRESULT hr = pCollection-&gt;GetElement(index, &amp;pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk-&gt;QueryInterface(IID_PPV_ARGS(ppObj));
        pUnk-&gt;Release();
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
    HRESULT hr = MFCreateTranscodeProfile(&amp;pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get output media types for the Windows Media audio encoder.

    // Enumerate all codecs except for codecs with field-of-use restrictions.
    // Sort the results.

    DWORD dwFlags = 
        (MFT_ENUM_FLAG_ALL &amp; (~MFT_ENUM_FLAG_FIELDOFUSE)) | 
        MFT_ENUM_FLAG_SORTANDFILTER;

    hr = MFTranscodeGetAudioOutputAvailableTypes(MFAudioFormat_WMAudioV9, 
        dwFlags, NULL, &amp;pAvailableTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAvailableTypes-&gt;GetElementCount(&amp;dwMTCount);
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
    hr = GetCollectionObject(pAvailableTypes, 0, &amp;pAudioType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateAttributes(&amp;pAudioAttrs, 0);       
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioType-&gt;CopyAllItems(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the audio attributes on the profile.
    hr = pProfile-&gt;SetAudioAttributes(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the container attributes.
    hr = MFCreateAttributes(&amp;pContainer, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pContainer-&gt;SetGUID(MF_TRANSCODE_CONTAINERTYPE, MFTranscodeContainerType_ASF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile-&gt;SetContainerAttributes(pContainer);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppProfile = pProfile;
    (*ppProfile)-&gt;AddRef();

done:
    SafeRelease(&amp;pProfile);
    SafeRelease(&amp;pAvailableTypes);
    SafeRelease(&amp;pAudioType);
    SafeRelease(&amp;pAudioAttrs);
    SafeRelease(&amp;pContainer);
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/82e012e0-84d8-4791-8b6f-bda58b498a90">IMFTranscodeProfile</a>



<a href="https://msdn.microsoft.com/8750eacb-7e6f-4c17-987b-f4baa4eea847">MFTranscodeGetAudioOutputAvailableTypes</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/24bf68a8-39bf-4302-b28c-71bb23b63469">Transcode API</a>
 

 

