---
UID: NF:wincodec.WICConvertBitmapSource
title: WICConvertBitmapSource function
author: windows-sdk-content
description: Obtains a IWICBitmapSource in the desired pixel format from a given IWICBitmapSource.
old-location: wic\_wic_codec_wicconvertbitmapsource.htm
old-project: wic
ms.assetid: ea735296-1bfd-4175-b8c9-cb5a61ab4203
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WICConvertBitmapSource, WICConvertBitmapSource function [Windows Imaging Component], _wic_codec_wicconvertbitmapsource, wic._wic_codec_wicconvertbitmapsource, wincodec/WICConvertBitmapSource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WICTiffCompressionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Windowscodecs.dll
 - Wincodec.lib
api_name:
 - WICConvertBitmapSource
product: Windows
targetos: Windows
req.lib: 
req.dll: Windowscodecs.dll; Wincodec.lib
req.irql: 
req.product: Windows Address Book 5.0
---

# WICConvertBitmapSource function


## -description


Obtains a <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a> in the desired pixel format from a given <b>IWICBitmapSource</b>.


## -parameters




### -param dstFormat [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ee719797(v=VS.85).aspx">REFWICPixelFormatGUID</a></b>

The pixel format to convert to.


### -param pISrc [in]

Type: <b><a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>*</b>

The source bitmap.


### -param ppIDst [out]

Type: <b><a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>**</b>

A pointer to the <b>null</b>-initialized destination bitmap pointer.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the <i>pISrc</i> bitmap is already in the desired format, <i>pISrc</i> is copied to the destination bitmap pointer and a reference is added. If it is not in the desired format however, <b>WICConvertBitmapSource</b> will instantiate a <i>dstFormat</i> format converter and initialize it with <i>pISrc</i>.


#### Examples

The following example converts an <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a> to a <b>GUID_WICPixelFormat128bppPRGBAFloat</b> pixel format.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
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
                    (LPVOID*) &amp;pFactory);

   // Create a decoder from the file.
   if (SUCCEEDED(hr))
   {
      hr = pFactory-&gt;CreateDecoderFromFilename(L"test.jpg",
                         NULL,
                         GENERIC_READ,
                         WICDecodeMetadataCacheOnDemand,
                         &amp;pDecoder);
   }

   // Get the frame count.
   if (SUCCEEDED(hr))
   {
      hr = pDecoder-&gt;GetFrameCount(&amp;uiFrameCount);
   }

   if (SUCCEEDED(hr) &amp;&amp; (uiFrameCount &gt; 0))
   {
      IWICBitmapSource *pSource = NULL;

      hr = pDecoder-&gt;GetFrame(0, &amp;pBitmapFrameDecode);

      if (SUCCEEDED(hr))
      {
         pSource = pBitmapFrameDecode;
         pSource-&gt;AddRef();

         hr = pSource-&gt;GetSize(&amp;uiWidth, &amp;uiHeight);
      }

      if (SUCCEEDED(hr))
      {
         hr = pSource-&gt;GetPixelFormat(&amp;pixelFormat);
      }

      if (SUCCEEDED(hr))
      {
         if (!IsEqualGUID(pixelFormat, GUID_WICPixelFormat128bppPRGBAFloat))
         {

            hr = WICConvertBitmapSource(GUID_WICPixelFormat128bppPRGBAFloat, pSource, &amp;pConverter);

            if (SUCCEEDED(hr))
            {
               pSource-&gt;Release();     // the converter has a reference to the source
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

               for (UINT i = 0; SUCCEEDED(hr) &amp;&amp; i &lt; uiHeight; i++)
               {
                  hr = pSource-&gt;CopyPixels(&amp;rc,
                                    cbStride,
                                    cbBufferSize,
                                    reinterpret_cast&lt;BYTE*&gt;(pixels));

                  // Do something with the scanline here...

                  rc.Y++;
               }

               delete[] pixels;
            }
            else
            {
               hr = E_OUTOFMEMORY;
            }

            pConverter-&gt;Release();
         }
      }
   }

   if (pBitmapFrameDecode)
   {
      pBitmapFrameDecode-&gt;Release();
   }

   if (pDecoder)
   {
      pDecoder-&gt;Release();
   }

   if (pFactory)
   {
      pFactory-&gt;Release();
   }

   return hr;</pre>
</td>
</tr>
</table></span></div>


