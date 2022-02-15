---
UID: NF:wincodec.IWICStream.InitializeFromFilename
title: IWICStream::InitializeFromFilename (wincodec.h)
description: Initializes a stream from a particular file.
helpviewer_keywords: ["GENERIC_READ","GENERIC_WRITE","IWICStream interface [Windows Imaging Component]","InitializeFromFilename method","IWICStream.InitializeFromFilename","IWICStream::InitializeFromFilename","InitializeFromFilename","InitializeFromFilename method [Windows Imaging Component]","InitializeFromFilename method [Windows Imaging Component]","IWICStream interface","_wic_codec_iwicstream_initializefromfilename","wic._wic_codec_iwicstream_initializefromfilename","wincodec/IWICStream::InitializeFromFilename"]
old-location: wic\_wic_codec_iwicstream_initializefromfilename.htm
tech.root: wic
ms.assetid: b0942d23-9c49-4726-9d84-bf0d448124b3
ms.date: 12/05/2018
ms.keywords: GENERIC_READ, GENERIC_WRITE, IWICStream interface [Windows Imaging Component],InitializeFromFilename method, IWICStream.InitializeFromFilename, IWICStream::InitializeFromFilename, InitializeFromFilename, InitializeFromFilename method [Windows Imaging Component], InitializeFromFilename method [Windows Imaging Component],IWICStream interface, _wic_codec_iwicstream_initializefromfilename, wic._wic_codec_iwicstream_initializefromfilename, wincodec/IWICStream::InitializeFromFilename
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
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICStream::InitializeFromFilename
 - wincodec/IWICStream::InitializeFromFilename
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICStream.InitializeFromFilename
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicstream">IWICStream</a> interface methods do not enable you to provide a file sharing option.
            To create a shared file stream for an image, use the <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shcreatestreamonfileex">SHCreateStreamOnFileEx</a> function.
            This stream can then be used to create an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a> using the <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream">CreateDecoderFromStream</a> method.
         


#### Examples

This example demonstrates the use of the <b>InitializeFromFilename</b> to create an image decoder.


```cpp
    IWICImagingFactory *pFactory = NULL;
    IWICStream *pStream = NULL;
    IWICBitmapDecoder *pDecoder = NULL;

    HRESULT hr = CoCreateInstance(
                    CLSID_WICImagingFactory,
                    NULL,
                    CLSCTX_INPROC_SERVER,
                    IID_PPV_ARGS(&pFactory));

    // Create the stream.
    if (SUCCEEDED(hr))
    {
        hr = pFactory->CreateStream(&pStream);
    }

    // Initialize the stream from a specific file.
    if (SUCCEEDED(hr))
    {
        hr = pStream->InitializeFromFilename(L"test.jpg", GENERIC_READ);
    }    

    // Create a JPEG decoder.
    // Since the stream is created from the JPEG file, an explicit JPEG decoder
    // can be created using the generic IWICImagingFactory::CreateDecoder method.
    // However, use IWICImagingFactory::CreateDecoderFromStream method to auto
    // detect the stream and instantiate the appropriate codec.  
    if (SUCCEEDED(hr))
    {        
        hr = pFactory->CreateDecoder(
                GUID_ContainerFormatJpeg,   // Explicitly create a JPEG decoder.
                NULL,                       // No preferred vendor.
                &pDecoder);                 // Pointer to the decoder.
    } 

    // Initialize the decoder
    if (SUCCEEDED(hr))
    {
        hr = pDecoder->Initialize(
                pStream,                            // The stream to use.
                WICDecodeMetadataCacheOnDemand);    // Decode metadata when needed.
    } 

    // Process image frame.
    if (SUCCEEDED(hr))
    {
        UINT cFrames = 0;

        hr = pDecoder->GetFrameCount(&cFrames);

        if (SUCCEEDED(hr) && (cFrames > 0))
        {
            UINT width = 0, height = 0;        
            IWICBitmapFrameDecode *pBitmapFrame = NULL;

            hr = pDecoder->GetFrame(0, &pBitmapFrame);

            if (SUCCEEDED(hr))
            {
                // Do something with the frame here.
            }

            if (pBitmapFrame)
            {
                pBitmapFrame->Release();
            }
        }
    } 

    if (pStream)
    {
        pStream->Release();
    }

    if (pFactory)
    {
        pFactory->Release();
    }

    if (pDecoder)
    {
        pDecoder->Release();
    }
```