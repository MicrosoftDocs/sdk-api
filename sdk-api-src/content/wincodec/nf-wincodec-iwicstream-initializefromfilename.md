---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
            To create a shared file stream for an image, use the <a href="_shell_SHCreateStreamOnFileEx">SHCreateStreamOnFileEx</a> function.
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


