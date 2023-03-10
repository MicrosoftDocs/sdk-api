---
UID: NF:wincodec.WICConvertBitmapSource
title: WICConvertBitmapSource function (wincodec.h)
description: Obtains a IWICBitmapSource in the desired pixel format from a given IWICBitmapSource.
helpviewer_keywords: ["WICConvertBitmapSource","WICConvertBitmapSource function [Windows Imaging Component]","_wic_codec_wicconvertbitmapsource","wic._wic_codec_wicconvertbitmapsource","wincodec/WICConvertBitmapSource"]
old-location: wic\_wic_codec_wicconvertbitmapsource.htm
tech.root: wic
ms.assetid: ea735296-1bfd-4175-b8c9-cb5a61ab4203
ms.date: 12/05/2018
ms.keywords: WICConvertBitmapSource, WICConvertBitmapSource function [Windows Imaging Component], _wic_codec_wicconvertbitmapsource, wic._wic_codec_wicconvertbitmapsource, wincodec/WICConvertBitmapSource
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - WICConvertBitmapSource
 - wincodec/WICConvertBitmapSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Windowscodecs.dll
 - Windowscodecs.lib
api_name:
 - WICConvertBitmapSource
---

## -description

Obtains a <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> in the desired pixel format from a given <b>IWICBitmapSource</b>.

## -parameters

### -param dstFormat [in]

Type: <b><a href="/windows/desktop/wic/-wic-codec-native-pixel-formats">REFWICPixelFormatGUID</a></b>

The pixel format to convert to.

### -param pISrc [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>*</b>

The source bitmap.

### -param ppIDst [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>**</b>

A pointer to the <b>null</b>-initialized destination bitmap pointer.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

If the <i>pISrc</i> bitmap is already in the desired format, then <i>pISrc</i> is copied to the destination bitmap pointer and a reference is added. If it is not in the desired format however, <b>WICConvertBitmapSource</b> will instantiate a <i>dstFormat</i> format converter and initialize it with <i>pISrc</i>.

## Examples

The following example converts an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> to a <b>GUID_WICPixelFormat128bppPRGBAFloat</b> pixel format.

```cpp
   IWICImagingFactory *pFactory = NULL;
   IWICBitmapDecoder *pDecoder = NULL;
   IWICBitmapFrameDecode *pBitmapFrameDecode = NULL;
   IWICBitmapSource *pConverter = NULL;

   UINT uiFrameCount = 0;
   UINT uiWidth = 0, uiHeight = 0;
   WICPixelFormatGUID pixelFormat;    

   // Create the image factory.
   HRESULT hr = CoCreateInstance(CLSID_WICImagingFactory,
                    NULL,
                    CLSCTX_INPROC_SERVER,
                    IID_IWICImagingFactory,
                    (LPVOID*) &pFactory);

   // Create a decoder from the file.
   if (SUCCEEDED(hr))
   {
      hr = pFactory->CreateDecoderFromFilename(L"test.jpg",
                         NULL,
                         GENERIC_READ,
                         WICDecodeMetadataCacheOnDemand,
                         &pDecoder);
   }

   // Get the frame count.
   if (SUCCEEDED(hr))
   {
      hr = pDecoder->GetFrameCount(&uiFrameCount);
   }

   if (SUCCEEDED(hr) && (uiFrameCount > 0))
   {
      IWICBitmapSource *pSource = NULL;

      hr = pDecoder->GetFrame(0, &pBitmapFrameDecode);

      if (SUCCEEDED(hr))
      {
         pSource = pBitmapFrameDecode;
         pSource->AddRef();

         hr = pSource->GetSize(&uiWidth, &uiHeight);
      }

      if (SUCCEEDED(hr))
      {
         hr = pSource->GetPixelFormat(&pixelFormat);
      }

      if (SUCCEEDED(hr))
      {
         if (!IsEqualGUID(pixelFormat, GUID_WICPixelFormat128bppPRGBAFloat))
         {

            hr = WICConvertBitmapSource(GUID_WICPixelFormat128bppPRGBAFloat, pSource, &pConverter);

            if (SUCCEEDED(hr))
            {
               pSource->Release();     // the converter has a reference to the source
               pSource = NULL;         // so we don't need it anymore.
               pSource = pConverter;   // let's treat the 128bppPABGR converter as the source
            }
         }

         if (piConverter)
         {
            UINT cbStride = uiWidth * sizeof(float) * 4;
            UINT cbBufferSize = cbStride;

            float *pixels = new float[cbBufferSize / sizeof(float)];

            if (pixels)
            {                    
               WICRect rc;
               rc.X = 0;
               rc.Y = 0;
               rc.Width = uiWidth;
               rc.Height = 1;

               for (UINT i = 0; SUCCEEDED(hr) && i < uiHeight; i++)
               {
                  hr = pSource->CopyPixels(&rc,
                                    cbStride,
                                    cbBufferSize,
                                    reinterpret_cast<BYTE*>(pixels));

                  // Do something with the scanline here...

                  rc.Y++;
               }

               delete[] pixels;
            }
            else
            {
               hr = E_OUTOFMEMORY;
            }

            pConverter->Release();
         }
      }
   }

   if (pBitmapFrameDecode)
   {
      pBitmapFrameDecode->Release();
   }

   if (pDecoder)
   {
      pDecoder->Release();
   }

   if (pFactory)
   {
      pFactory->Release();
   }

   return hr;
```

