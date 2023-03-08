---
UID: NF:wincodec.IWICColorTransform.Initialize
title: IWICColorTransform::Initialize (wincodec.h)
description: Initializes an IWICColorTransform with a IWICBitmapSource and transforms it from one IWICColorContext to another.
helpviewer_keywords: ["IWICColorTransform interface [Windows Imaging Component]","Initialize method","IWICColorTransform.Initialize","IWICColorTransform::Initialize","Initialize","Initialize method [Windows Imaging Component]","Initialize method [Windows Imaging Component]","IWICColorTransform interface","_wic_codec_iwiccolortransform_initialize","wic._wic_codec_iwiccolortransform_initialize","wincodec/IWICColorTransform::Initialize"]
old-location: wic\_wic_codec_iwiccolortransform_initialize.htm
tech.root: wic
ms.assetid: 572a014b-10f9-4b76-9090-04ac13edfc3d
ms.date: 12/05/2018
ms.keywords: IWICColorTransform interface [Windows Imaging Component],Initialize method, IWICColorTransform.Initialize, IWICColorTransform::Initialize, Initialize, Initialize method [Windows Imaging Component], Initialize method [Windows Imaging Component],IWICColorTransform interface, _wic_codec_iwiccolortransform_initialize, wic._wic_codec_iwiccolortransform_initialize, wincodec/IWICColorTransform::Initialize
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
 - IWICColorTransform::Initialize
 - wincodec/IWICColorTransform::Initialize
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
 - IWICColorTransform.Initialize
---

# IWICColorTransform::Initialize


## -description

Initializes an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolortransform">IWICColorTransform</a> with a <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> and transforms it from one <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a> to another.

## -parameters

### -param pIBitmapSource [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>*</b>

The bitmap source used to initialize the color transform.

### -param pIContextSource [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a>*</b>

The color context source.

### -param pIContextDest [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a>*</b>

The color context destination.

### -param pixelFmtDest [in]

Type: <b>REFWICPixelFormatGUID</b>

The GUID of the desired pixel format.

This parameter is limited to a subset of the native WIC pixel formats, see Remarks for a list.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The currently supported formats for the <i>pIContextSource</i>  and <i>pixelFmtDest</i> parameters are: 


<ul>
<li>GUID_WICPixelFormat8bppGray</li>
<li>GUID_WICPixelFormat16bppGray</li>
<li>GUID_WICPixelFormat16bppBGR555</li>
<li>GUID_WICPixelFormat16bppBGR565</li>
<li>GUID_WICPixelFormat24bppBGR</li>
<li>GUID_WICPixelFormat24bppRGB</li>
<li>GUID_WICPixelFormat32bppBGR</li>
<li>GUID_WICPixelFormat32bppBGRA</li>
<li>GUID_WICPixelFormat32bppPBGRA</li>
<li>GUID_WICPixelFormat32bppPRGBA (Windows 8 and later)</li>
<li>GUID_WICPixelFormat32bppRGBA</li>
<li>GUID_WICPixelFormat32bppBGR101010</li>
<li>GUID_WICPixelFormat32bppCMYK</li>
<li>GUID_WICPixelFormat48bppBGR</li>
<li>GUID_WICPixelFormat64bppBGRA 		(Windows 8 and later)</li>
<li>GUID_WICPixelFormat64bppPBGRA (Windows 8 and later)</li>
<li>GUID_WICPixelFormat64bppPRGBA (Windows 8 and later)</li>
<li>GUID_WICPixelFormat64bppRGBA 		 (Windows 8 and later)</li>
</ul>
In order to get correct behavior from a color transform, the input and output pixel formats must be compatible with the source and destination color profiles. For example, an sRGB destination color profile will produce incorrect results when used with a CMYK destination pixel format.


#### Examples

The following example performs a color transform from one <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a> to another.


```cpp

    IWICImagingFactory *pFactory = NULL;
    IWICBitmapDecoder *pDecoder = NULL;
    IWICBitmapFrameDecode *pBitmapFrame = NULL;
    IWICColorContext *pContextSrc = NULL;
    IWICColorContext *pContextDst = NULL;
    IWICColorTransform *pColorTransform = NULL;

    UINT uiFrameCount = 0;

    HRESULT hr = CoCreateInstance(
                    CLSID_WICImagingFactory,
                    NULL, CLSCTX_INPROC_SERVER,
                    IID_IWICImagingFactory,
                    (LPVOID*) &pFactory);

    if (SUCCEEDED(hr))
    {
        hr = pFactory->CreateDecoderFromFilename(
                           L"test.jpg",
                           NULL,
                           GENERIC_READ,
                           WICDecodeMetadataCacheOnDemand,
                           &pDecoder);
    }

    if (SUCCEEDED(hr))
    {
        hr = pDecoder->GetFrameCount(&uiFrameCount);
    }

    if (SUCCEEDED(hr) && (uiFrameCount > 0))
    {
        hr = pDecoder->GetFrame(0, &piBitmapFrame);
    }

    if (SUCCEEDED(hr))
    {
        hr = pFactory->CreateColorContext(&pContextSrc);
    }

    if (SUCCEEDED(hr))
    {
        hr = pContextSrc->InitializeFromFilename(
                              L"c:\\windows\\system32\\spool\\drivers\\color\\kodak_dc.icm");
    }

    if (SUCCEEDED(hr))
    {
        hr = pFactory->CreateColorContext(&pContextDst);
    }

    if (SUCCEEDED(hr))
    {
        hr = pContextDst->InitializeFromFilename(
                              L"c:\\windows\\system32\\spool\\drivers\\color\\sRGB Color Space Profile.icm");
    }

    hr = E_FAIL;

    if (SUCCEEDED(hr))
    {
        // Transform from src icm to the destination icm. 
        hr = pColorTransform->Initialize( pBitmapFrame,
                                          pContextSrc,
                                          pContextDst,
                                          GUID_WICPixelFormat32bppBGRA);
    }

    if (SUCCEEDED(hr))
    {
        UINT uiWidth = 0, uiHeight = 0;
        UINT cbStride = 0;
        UINT cbBufferSize = 0;
        BYTE *pbBuffer = NULL; 

        hr = pColorTransform->GetSize(&uiWidth, &uiHeight);

        if (SUCCEEDED(hr))
        {
            WICRect rc = { 0 };
            rc.X = 0;
            rc.Y = 0;
            rc.Width = uiWidth;
            rc.Height = 1; // scanline

            for (UINT i = 0; SUCCEEDED(hr) && (i < uiHeight); i++)
            {
                hr = pColorTransform->CopyPixels(&rc, cbStride, cbBufferSize - (rc.Y * cbStride), pbBuffer);
                pbBuffer += cbStride;
                rc.Y += 1;
            }
        }
    }

    if (pFactory)
    {
        pFactory->Release();
    }

    if (pDecoder)
    {
        pDecoder->Release();
    }

    if (pBitmapFrame)
    {
        pBitmapFrame->Release();
    }

    if (pContextSrc)
    {
        pContextSrc->Release();
    }

    if (pContextDst)
    {
        pContextDst->Release();
    }

    if (pColorTransform)
    {
        pColorTransform->Release();
    }

    return hr;

```