---
UID: NF:wincodec.IWICBitmap.Lock
title: IWICBitmap::Lock
author: windows-sdk-content
description: Provides access to a rectangular area of the bitmap.
old-location: wic\_wic_codec_iwicbitmap_lock.htm
old-project: wic
ms.assetid: 2ab25a00-c89c-4a2c-8e12-8ce81cc21bca
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IWICBitmap interface [Windows Imaging Component],Lock method, IWICBitmap.Lock, IWICBitmap::Lock, Lock, Lock method [Windows Imaging Component], Lock method [Windows Imaging Component],IWICBitmap interface, WICBitmapLockRead, WICBitmapLockWrite, _wic_codec_iwicbitmap_lock, wic._wic_codec_iwicbitmap_lock, wincodec/IWICBitmap::Lock
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
 - IWICBitmap.Lock
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmap::Lock


## -description


Provides access to a rectangular area of the bitmap.


## -parameters




### -param prcLock [in]

Type: <b>const <a href="https://msdn.microsoft.com/e07c26bf-b645-4382-bb93-8472ba397026">WICRect</a>*</b>

The rectangle to be accessed.


### -param flags [in]

Type: <b>DWORD</b>

The access mode you wish to obtain for the lock. This is a bitwise combination of <a href="https://msdn.microsoft.com/d4d1bb38-3d1a-4e1e-a889-0491f3c01822">WICBitmapLockFlags</a> for read, write, or read and write access.

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

Type: <b><a href="https://msdn.microsoft.com/c0ddbc25-6abe-484b-a545-3b9376c514df">IWICBitmapLock</a>**</b>

A pointer that receives the locked memory location.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Locks are exclusive for writing but can be shared for reading. You cannot call <a href="https://msdn.microsoft.com/d4908a75-e7de-4b8f-bdc8-d86cf6b49f8c">CopyPixels</a> while the <a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a> is locked for writing. Doing so will return an error, since locks are exclusive.


#### Examples




         	In the following example, an <a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a> is created and the image data is cleared using an <a href="https://msdn.microsoft.com/c0ddbc25-6abe-484b-a545-3b9376c514df">IWICBitmapLock</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>

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
        (LPVOID*)&amp;pFactory
        );

    if (SUCCEEDED(hr))
    {
        hr = pFactory-&gt;CreateBitmap(uiWidth, uiHeight, formatGUID, WICBitmapCacheOnDemand, &amp;pBitmap);
    }

    if (SUCCEEDED(hr))
    {
        hr = pBitmap-&gt;Lock(&amp;rcLock, WICBitmapLockWrite, &amp;pLock);

        if (SUCCEEDED(hr))
        {
            UINT cbBufferSize = 0;
            UINT cbStride = 0;
            BYTE *pv = NULL;

            hr = pLock-&gt;GetStride(&amp;cbStride);

            if (SUCCEEDED(hr))
            {
                hr = pLock-&gt;GetDataPointer(&amp;cbBufferSize, &amp;pv);
            }

            // Clear the image data
            ZeroMemory(pv, cbBufferSize);

            // Release the bitmap lock.
            pLock-&gt;Release();
        }
    }

    if (pBitmap)
    {
        pBitmap-&gt;Release();
    }

    if (pFactory)
    {
        pFactory-&gt;Release();
    }

    return hr;
</pre>
</td>
</tr>
</table></span></div>


