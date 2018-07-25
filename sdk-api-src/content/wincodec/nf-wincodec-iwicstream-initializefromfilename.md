---
UID: NF:wincodec.IWICStream.InitializeFromFilename
title: IWICStream::InitializeFromFilename
author: windows-sdk-content
description: Initializes a stream from a particular file.
old-location: wic\_wic_codec_iwicstream_initializefromfilename.htm
old-project: wic
ms.assetid: b0942d23-9c49-4726-9d84-bf0d448124b3
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GENERIC_READ, GENERIC_WRITE, IWICStream interface [Windows Imaging Component],InitializeFromFilename method, IWICStream.InitializeFromFilename, IWICStream::InitializeFromFilename, InitializeFromFilename, InitializeFromFilename method [Windows Imaging Component], InitializeFromFilename method [Windows Imaging Component],IWICStream interface, _wic_codec_iwicstream_initializefromfilename, wic._wic_codec_iwicstream_initializefromfilename, wincodec/IWICStream::InitializeFromFilename
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WICTiffCompressionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICStream.InitializeFromFilename
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICStream::InitializeFromFilename


## -description


Initializes a stream from a particular file.


## -parameters




### -param wzFileName [in]

Type: <b>LPCWSTR</b>

The file used to initialize the stream.


### -param dwDesiredAccess [in]

Type: <b>DWORD</b>

The desired file access mode.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GENERIC_READ"></a><a id="generic_read"></a><dl>
<dt><b>GENERIC_READ</b></dt>
</dl>
</td>
<td width="60%">
Read access.

</td>
</tr>
<tr>
<td width="40%"><a id="GENERIC_WRITE"></a><a id="generic_write"></a><dl>
<dt><b>GENERIC_WRITE</b></dt>
</dl>
</td>
<td width="60%">
Write access.

</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




            The <a href="https://msdn.microsoft.com/bc398732-037d-4f48-940f-c70975447972">IWICStream</a> interface methods do not enable you to provide a file sharing option.
            To create a shared file stream for an image, use the <a href="https://msdn.microsoft.com/library/Bb759866(v=VS.85).aspx">SHCreateStreamOnFileEx</a> function.
            This stream can then be used to create an <a href="https://msdn.microsoft.com/91dafd5e-e4fb-4691-a3d0-ca8b6ff0aaf7">IWICBitmapDecoder</a> using the <a href="https://msdn.microsoft.com/b9328715-54a0-4c9a-9977-3252068b7e4b">CreateDecoderFromStream</a> method.
         


#### Examples

This example demonstrates the use of the <b>InitializeFromFilename</b> to create an image decoder.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    IWICImagingFactory *pFactory = NULL;
    IWICStream *pStream = NULL;
    IWICBitmapDecoder *pDecoder = NULL;

    HRESULT hr = CoCreateInstance(
                    CLSID_WICImagingFactory,
                    NULL,
                    CLSCTX_INPROC_SERVER,
                    IID_PPV_ARGS(&amp;pFactory));

    // Create the stream.
    if (SUCCEEDED(hr))
    {
        hr = pFactory-&gt;CreateStream(&amp;pStream);
    }

    // Initialize the stream from a specific file.
    if (SUCCEEDED(hr))
    {
        hr = pStream-&gt;InitializeFromFilename(L"test.jpg", GENERIC_READ);
    }    

    // Create a JPEG decoder.
    // Since the stream is created from the JPEG file, an explicit JPEG decoder
    // can be created using the generic IWICImagingFactory::CreateDecoder method.
    // However, use IWICImagingFactory::CreateDecoderFromStream method to auto
    // detect the stream and instantiate the appropriate codec.  
    if (SUCCEEDED(hr))
    {        
        hr = pFactory-&gt;CreateDecoder(
                GUID_ContainerFormatJpeg,   // Explicitly create a JPEG decoder.
                NULL,                       // No preferred vendor.
                &amp;pDecoder);                 // Pointer to the decoder.
    } 

    // Initialize the decoder
    if (SUCCEEDED(hr))
    {
        hr = pDecoder-&gt;Initialize(
                pStream,                            // The stream to use.
                WICDecodeMetadataCacheOnDemand);    // Decode metadata when needed.
    } 

    // Process image frame.
    if (SUCCEEDED(hr))
    {
        UINT cFrames = 0;

        hr = pDecoder-&gt;GetFrameCount(&amp;cFrames);

        if (SUCCEEDED(hr) &amp;&amp; (cFrames &gt; 0))
        {
            UINT width = 0, height = 0;        
            IWICBitmapFrameDecode *pBitmapFrame = NULL;

            hr = pDecoder-&gt;GetFrame(0, &amp;pBitmapFrame);

            if (SUCCEEDED(hr))
            {
                // Do something with the frame here.
            }

            if (pBitmapFrame)
            {
                pBitmapFrame-&gt;Release();
            }
        }
    } 

    if (pStream)
    {
        pStream-&gt;Release();
    }

    if (pFactory)
    {
        pFactory-&gt;Release();
    }

    if (pDecoder)
    {
        pDecoder-&gt;Release();
    }</pre>
</td>
</tr>
</table></span></div>


