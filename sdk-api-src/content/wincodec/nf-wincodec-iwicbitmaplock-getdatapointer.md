---
UID: NF:wincodec.IWICBitmapLock.GetDataPointer
title: IWICBitmapLock::GetDataPointer (wincodec.h)
description: Gets the pointer to the top left pixel in the locked rectangle.
helpviewer_keywords: ["GetDataPointer","GetDataPointer method [Windows Imaging Component]","GetDataPointer method [Windows Imaging Component]","IWICBitmapLock interface","IWICBitmapLock interface [Windows Imaging Component]","GetDataPointer method","IWICBitmapLock.GetDataPointer","IWICBitmapLock::GetDataPointer","_wic_codec_iwicbitmaplock_getdatapointer","wic._wic_codec_iwicbitmaplock_getdatapointer","wincodec/IWICBitmapLock::GetDataPointer"]
old-location: wic\_wic_codec_iwicbitmaplock_getdatapointer.htm
tech.root: wic
ms.assetid: 1fae52ae-b410-48f3-be46-624792f96874
ms.date: 12/05/2018
ms.keywords: GetDataPointer, GetDataPointer method [Windows Imaging Component], GetDataPointer method [Windows Imaging Component],IWICBitmapLock interface, IWICBitmapLock interface [Windows Imaging Component],GetDataPointer method, IWICBitmapLock.GetDataPointer, IWICBitmapLock::GetDataPointer, _wic_codec_iwicbitmaplock_getdatapointer, wic._wic_codec_iwicbitmaplock_getdatapointer, wincodec/IWICBitmapLock::GetDataPointer
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
 - IWICBitmapLock::GetDataPointer
 - wincodec/IWICBitmapLock::GetDataPointer
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
 - IWICBitmapLock.GetDataPointer
---

# IWICBitmapLock::GetDataPointer


## -description

Gets the pointer to the top left pixel in the locked rectangle.

## -parameters

### -param pcbBufferSize [out]

Type: <b>UINT*</b>

A pointer that receives the size of the buffer.

### -param ppbData [out]

Type: <b>BYTE**</b>

A pointer that receives a pointer to the top left pixel in the locked rectangle.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The pointer provided by this method should not be used outside of the lifetime of the lock itself.

<b>GetDataPointer</b> is not available in multi-threaded apartment applications.


#### Examples

In the following example, the data pointed to by the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmaplock">IWICBitmapLock</a> is zeroed.


```cpp

    IWICImagingFactory *pFactory = NULL;
    IWICBitmap *pBitmap = NULL;

    UINT uiWidth = 640;
    UINT uiHeight = 480;
    WICPixelFormatGUID formatGUID = GUID_WICPixelFormat32bppARGB;

    WICRect rcLock = { 0, 0, uiWidth, uiHeight };
    IWICBitmapLock *pLock = NULL;

    HRESULT hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWICImagingFactory,
        (LPVOID*)&pFactory
        );

    if (SUCCEEDED(hr))
    {
        hr = pFactory->CreateBitmap(uiWidth, uiHeight, formatGUID, WICBitmapCacheOnDemand, &pBitmap);
    }

    if (SUCCEEDED(hr))
    {
        hr = pBitmap->Lock(&rcLock, WICBitmapLockWrite, &pLock);

        if (SUCCEEDED(hr))
        {
            UINT cbBufferSize = 0;
            UINT cbStride = 0;
            BYTE *pv = NULL;

            // Retrieve the stride.
            hr = pLock->GetStride(&cbStride);

            if (SUCCEEDED(hr))
            {
                hr = pLock->GetDataPointer(&cbBufferSize, &pv);
            }
            if (SUCCEEDED(hr))
            {
                // Access the bitmap memory starting at pv, where
                // each row begins cbStride bytes after the start
                // of the preceding row.
            }

            // Release the bitmap lock.
            pLock->Release();
        }
    }

    if (pBitmap)
    {
        pBitmap->Release();
    }

    if (pFactory)
    {
        pFactory->Release();
    }

    return hr;

```