---
UID: NF:wincodec.IWICBitmap.Lock
title: IWICBitmap::Lock (wincodec.h)
description: Provides access to a rectangular area of the bitmap.
helpviewer_keywords: ["IWICBitmap interface [Windows Imaging Component]","Lock method","IWICBitmap.Lock","IWICBitmap::Lock","Lock","Lock method [Windows Imaging Component]","Lock method [Windows Imaging Component]","IWICBitmap interface","WICBitmapLockRead","WICBitmapLockWrite","_wic_codec_iwicbitmap_lock","wic._wic_codec_iwicbitmap_lock","wincodec/IWICBitmap::Lock"]
old-location: wic\_wic_codec_iwicbitmap_lock.htm
tech.root: wic
ms.assetid: 2ab25a00-c89c-4a2c-8e12-8ce81cc21bca
ms.date: 12/05/2018
ms.keywords: IWICBitmap interface [Windows Imaging Component],Lock method, IWICBitmap.Lock, IWICBitmap::Lock, Lock, Lock method [Windows Imaging Component], Lock method [Windows Imaging Component],IWICBitmap interface, WICBitmapLockRead, WICBitmapLockWrite, _wic_codec_iwicbitmap_lock, wic._wic_codec_iwicbitmap_lock, wincodec/IWICBitmap::Lock
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
 - IWICBitmap::Lock
 - wincodec/IWICBitmap::Lock
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
 - IWICBitmap.Lock
---

# IWICBitmap::Lock


## -description

Provides access to a rectangular area of the bitmap.

## -parameters

### -param prcLock [in]

Type: <b>const <a href="/windows/desktop/api/wincodec/ns-wincodec-wicrect">WICRect</a>*</b>

The rectangle to be accessed.

### -param flags [in]

Type: <b>DWORD</b>

The access mode you wish to obtain for the lock. This is a bitwise combination of <a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmaplockflags">WICBitmapLockFlags</a> for read, write, or read and write access.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WICBitmapLockRead"></a><a id="wicbitmaplockread"></a><a id="WICBITMAPLOCKREAD"></a><dl>
<dt><b>WICBitmapLockRead</b></dt>
</dl>
</td>
<td width="60%">
The read access lock.

</td>
</tr>
<tr>
<td width="40%"><a id="WICBitmapLockWrite"></a><a id="wicbitmaplockwrite"></a><a id="WICBITMAPLOCKWRITE"></a><dl>
<dt><b>WICBitmapLockWrite</b></dt>
</dl>
</td>
<td width="60%">
The write access lock.

</td>
</tr>
</table>

### -param ppILock [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmaplock">IWICBitmapLock</a>**</b>

A pointer that receives the locked memory location.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Locks are exclusive for writing but can be shared for reading. You cannot call <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels">CopyPixels</a> while the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a> is locked for writing. Doing so will return an error, since locks are exclusive.


#### Examples



In the following example, an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a> is created and the image data is cleared using an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmaplock">IWICBitmapLock</a>.


```cpp


    IWICImagingFactory *pFactory = NULL;
    IWICBitmap *pBitmap = NULL;

    UINT uiWidth = 640;
    UINT uiHeight = 480;
    WICPixelFormatGUID formatGUID = GUID_WICPixelFormat32bppBGRA;

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

            hr = pLock->GetStride(&cbStride);

            if (SUCCEEDED(hr))
            {
                hr = pLock->GetDataPointer(&cbBufferSize, &pv);
            }

            // Clear the image data
            ZeroMemory(pv, cbBufferSize);

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