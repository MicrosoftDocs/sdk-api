---
UID: NF:wmcontainer.MFCreateASFStreamingMediaSink
title: MFCreateASFStreamingMediaSink function
author: windows-sdk-content
description: Creates an activation object for the ASF streaming sink.
old-location: mf\mfcreateasfstreamingmediasink.htm
old-project: medfound
ms.assetid: bfa34529-e1f9-462b-9c99-b65cd526d364
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: MFCreateASFStreamingMediaSink, MFCreateASFStreamingMediaSink function [Media Foundation], mf.mfcreateasfstreamingmediasink, wmcontainer/MFCreateASFStreamingMediaSink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: MFASF_STREAMSELECTOR_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateASFStreamingMediaSink
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# MFCreateASFStreamingMediaSink function


## -description


Creates an activation object for the ASF streaming sink.

The  ASF streaming sink enables  an application to write streaming Advanced Systems Format (ASF)  packets to an HTTP byte stream.
      


## -parameters




### -param pIByteStream

 A pointer to a byte stream object in which the ASF media sink writes the streamed content.


### -param ppIMediaSink

Receives a pointer to the <a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a> interface of the ASF streaming-media sink object. To create the media sink, the application must call <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">IMFActivate::ActivateObject</a> on the received pointer. The caller must release the interface pointer.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To create the ASF streaming sink in another process, call <a href="https://msdn.microsoft.com/ffcab5ee-400a-424f-ab98-3c9e36ef40ce">MFCreateASFStreamingMediaSinkActivate</a>.
      

An application can get a pointer to the <a href="https://msdn.microsoft.com/6b7f8b68-fe98-4aeb-9842-a80ac6235999">ASF ContentInfo Object</a> by calling <b>IUnknown::QueryInterface</b> on the media sink object received in the <i>ppIMediaSink</i> parameter. The ContentInfo object is used to set the encoder configuration settings, provide stream properties supplied by an ASF profile, and add metadata information. These configuration settings populate the various ASF header objects of the encoded ASF file. For more information, see  
<a href="https://msdn.microsoft.com/30e3c10b-1310-4194-8b83-221dfe73b03c">Setting Properties in the ContentInfo Object</a>.


#### Examples

The following code example shows how to create a media sink for an ASF source. This example copies the stream configuration settings from the source to the ContentInfo object that represents the ASF header object of the output file.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//  Creates an an instance of the ASF streaming sink.

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
    HRESULT hr = MFCreateASFStreamingMediaSink(pOutputByteStream, &amp;pMediaSink);
    if (FAILED(hr))
    {
        goto done;
    }

    //
    // Transfer the ASF profile from the media source to the sink.
    //

    // Get the presentation descriptor from the source.
    hr = pSource-&gt;CreatePresentationDescriptor(&amp;pSourcePD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Convert the presentation descriptor to an ASF profile.
    hr = MFCreateASFProfileFromPresentationDescriptor(pSourcePD, &amp;pASFProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pMediaSink-&gt;QueryInterface(IID_PPV_ARGS(&amp;pASFContentInfo));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the profile on the sink.
    hr = pASFContentInfo-&gt;SetProfile(pASFProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppMediaSink = pMediaSink;
    (*ppMediaSink)-&gt;AddRef();

done:
    SafeRelease(&amp;pSourcePD);
    SafeRelease(&amp;pASFProfile);
    SafeRelease(&amp;pASFContentInfo);
    SafeRelease(&amp;pMediaSink);
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ffcab5ee-400a-424f-ab98-3c9e36ef40ce">MFCreateASFStreamingMediaSinkActivate</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

