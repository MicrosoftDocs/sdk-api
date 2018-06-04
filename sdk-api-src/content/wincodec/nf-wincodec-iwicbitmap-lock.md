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


