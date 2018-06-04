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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The pointer provided by this method should not be used outside of the lifetime of the lock itself.

<b>GetDataPointer</b> is not available in multi-threaded apartment applications.


#### Examples

In the following example, the data pointed to by the <a href="https://msdn.microsoft.com/c0ddbc25-6abe-484b-a545-3b9376c514df">IWICBitmapLock</a> is zero'd.

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
    WICPixelFormatGUID formatGUID = GUID_WICPixelFormat32bppARGB;

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

            // Retrieve the stride.
            hr = pLock-&gt;GetStride(&amp;cbStride);

            if (SUCCEEDED(hr))
            {
                hr = pLock-&gt;GetDataPointer(&amp;cbBufferSize, &amp;pv);
            }
            if (SUCCEEDED(hr))
            {
                // Access the bitmap memory starting at pv, where
                // each row begins cbStride bytes after the start
                // of the preceding row.
            }

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


