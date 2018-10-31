---
UID: NN:mfidl.IMFTranscodeSinkInfoProvider
title: IMFTranscodeSinkInfoProvider
author: windows-sdk-content
description: Implemented by the transcode sink activation object.
old-location: mf\imftranscodesinkinfoprovider.htm
tech.root: medfound
ms.assetid: c5eb0c30-559a-44dd-80d4-4b11933dc7ce
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IMFTranscodeSinkInfoProvider, IMFTranscodeSinkInfoProvider interface [Media Foundation], IMFTranscodeSinkInfoProvider interface [Media Foundation],described, mf.imftranscodesinkinfoprovider, mfidl/IMFTranscodeSinkInfoProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTranscodeSinkInfoProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFTranscodeSinkInfoProvider</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d880e13a-879e-4882-a69d-f1920225e478">GetSinkInfo</a>
</td>
<td align="left" width="63%">
Gets the audio stream and the video stream attributes specified in the transcode profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/234bed82-a148-4313-a8cb-eefe2061b7ed">SetOutputByteStream</a>
</td>
<td align="left" width="63%">
Sets the output byte stream for the transcode media sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/048d1822-9349-4d49-a468-c89bc9c51583">SetOutputFile</a>
</td>
<td align="left" width="63%">
Sets the name of the output file to which the media sink writes the transcoded content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81137d8c-70b2-4a0a-a1b4-16a2f50f134b">SetProfile</a>
</td>
<td align="left" width="63%">
Sets the specified transcode profile that contains the configuration settings for the audio stream, the video stream, and the container to which the file is written.

</td>
</tr>
</table> 


## -remarks



To use this interface, perform the following steps:

<ol>
<li>Call <a href="https://msdn.microsoft.com/cc9c604d-7f5a-4afb-a2df-b270ef883e68">MFCreateTranscodeSinkActivate</a> to create the transcode sink activation object.</li>
<li>Query the activation object for the <b>IMFTranscodeSinkInfoProvider</b> interface.</li>
<li>Call <a href="https://msdn.microsoft.com/2a482c6f-6e20-419a-a7eb-085c41cc8186">MFCreateTranscodeProfile</a> to create a transcode profile.</li>
<li>Set the <a href="https://msdn.microsoft.com/97fd968a-6843-4695-aece-02f9acd618fd">MF_TRANSCODE_CONTAINERTYPE</a> attribute on the transcode profile. The attribute must have one of the following values:<ul>
<li><b>MFTranscodeContainerType_3GP</b></li>
<li><b>MFTranscodeContainerType_MP3</b></li>
<li><b>MFTranscodeContainerType_MPEG4</b></li>
</ul>
</li>
<li>Call <a href="https://msdn.microsoft.com/e68653c5-5663-4839-a482-2244e147f4b9">IMFTranscodeProfile::SetVideoAttributes</a> and <a href="https://msdn.microsoft.com/4118bb2b-8373-434a-896b-de5a1ba8c793">IMFTranscodeProfile::SetAudioAttributes</a> to specify the video and audio formats.</li>
<li>Call <a href="https://msdn.microsoft.com/81137d8c-70b2-4a0a-a1b4-16a2f50f134b">IMFTranscodeSinkInfoProvider::SetProfile</a> to set the transcode profile.</li>
<li>Call one of the following methods (but not both) to specify the output file:<ul>
<li>
<a href="https://msdn.microsoft.com/234bed82-a148-4313-a8cb-eefe2061b7ed">IMFTranscodeSinkInfoProvider::SetOutputByteStream</a>
</li>
<li>
<a href="https://msdn.microsoft.com/048d1822-9349-4d49-a468-c89bc9c51583">IMFTranscodeSinkInfoProvider::SetOutputFile</a>
</li>
</ul>
</li>
<li>Call <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">IMFActivate::ActivateObject</a> on the activation object to create the media sink.</li>
</ol>

#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Creates an activation object for the generic transcode sink.

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

    HRESULT hr = MFCreateAttributes(&amp;pContainerAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the transcode profile.
    hr = MFCreateTranscodeProfile(&amp;pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the profile attributes.

    hr = pContainerAttributes-&gt;SetGUID(MF_TRANSCODE_CONTAINERTYPE, guidContainerType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile-&gt;SetContainerAttributes(pContainerAttributes);
    if (FAILED(hr))
    {
        goto done;
    }

    if (pVideoAttributes)
    {
        hr = pProfile-&gt;SetVideoAttributes(pVideoAttributes);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    if (pAudioAttributes)
    {
        hr = pProfile-&gt;SetAudioAttributes(pAudioAttributes);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Create the transcode sink activation object.
    hr = MFCreateTranscodeSinkActivate(&amp;pSinkActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSinkActivate-&gt;QueryInterface(IID_PPV_ARGS(&amp;pSinkInfoProvider));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the output byte stream.
    hr = pSinkInfoProvider-&gt;SetOutputByteStream(pByteStreamActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the transcode profile.
    hr = pSinkInfoProvider-&gt;SetProfile(pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the activation object to the caller.
    *ppSinkActivate = pSinkActivate;
    (*ppSinkActivate)-&gt;AddRef();

done:
    SafeRelease(&amp;pProfile);
    SafeRelease(&amp;pSinkInfoProvider);
    SafeRelease(&amp;pSinkActivate);
    SafeRelease(&amp;pContainerAttributes);
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/cc9c604d-7f5a-4afb-a2df-b270ef883e68">MFCreateTranscodeSinkActivate</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

