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

# IMFVideoMixerBitmap::SetAlphaBitmap


## -description



Sets a bitmap image for the enhanced video renderer (EVR) to alpha-blend with the video.




## -parameters




### -param pBmpParms [in]

Pointer to an <a href="https://msdn.microsoft.com/609041f2-7ba4-4157-819b-4ac21612dca2">MFVideoAlphaBitmap</a> structure that contains information about the bitmap, the source and destination rectangles, the color key, and other information.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The blending parameters defined in the <i>pBmpParms</i> structure are not valid.

</td>
</tr>
</table>
 




## -remarks



The application can provide the image either as a GDI bitmap or as a Direct3D surface. The EVR mixer blends the image with the next video frame and all subsequent frames, until the image is changed or removed. The image can contain embedded per-pixel alpha information so that transparent regions can be defined. Transparent areas can also be identified using a color key value.

If you use a Direct3D surface, the surface format must be 32-bit RGB, either D3DFMT_X8R8G8B8 or D3DFMT_A8R8G8B8, and the surface must be allocated from the D3DPOOL_SYSTEMMEM memory pool.

There is no defined limit to how frequently you can pass images to the video renderer. However, changing the image several times per second can impact the performance and smoothness of the video.


#### Examples

The following example sets a GDI bitmap for alpha blending. For purposes of the example, it uses predefined settings for the destination rectangle and alpha value.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>HRESULT EVRPlayer::SetBitmapImage(BOOL bEnable, HBITMAP hBitmap)
{
    const float fBitmapAlpha = 0.5f; 

    HRESULT hr = S_OK;

    // To enable the bitmap, you must supply a valid bitmap handle.
    if (bEnable &amp;&amp; (hBitmap == NULL))
    {
        return E_INVALIDARG;
    }
    
    // Make sure we have an IMFVideoMixerBitmap pointer.
    if (m_pMixerBitmap == NULL)
    {
        return E_FAIL;
    }

    if (bEnable)
    {
        // Place the bitmap in the lower-right quadrant of the video.
        MFVideoNormalizedRect nrcDest = { 0.5f, 0.5f, 1.0f, 1.0f };

        // Get the device context for the video window.
        HDC hdc = GetDC(m_hwndVideo);

        // Create a compatible DC and select the bitmap into the DC&gt;
        HDC hdcBmp = CreateCompatibleDC(hdc);
        HBITMAP hOld = (HBITMAP)SelectObject(hdcBmp, hBitmap);

        // Fill in the blending parameters.
        MFVideoAlphaBitmap bmpInfo;
        ZeroMemory(&amp;bmpInfo, sizeof(bmpInfo));
        bmpInfo.GetBitmapFromDC = TRUE; // Use a bitmap DC (not a Direct3D surface).
        bmpInfo.bitmap.hdc = hdcBmp;
        bmpInfo.params.dwFlags = 
            MFVideoAlphaBitmap_Alpha | MFVideoAlphaBitmap_DestRect;
        bmpInfo.params.fAlpha = fBitmapAlpha;
        bmpInfo.params.nrcDest = nrcDest;

        // Get the bitmap dimensions.
        BITMAP bm;
        GetObject(hBitmap, sizeof(BITMAP), &amp;bm);

        // Set the source rectangle equal to the entire bitmap.
        SetRect(&amp;bmpInfo.params.rcSrc, 0, 0, bm.bmWidth, bm.bmHeight);

        // Set the bitmap.
        hr = m_pMixerBitmap-&gt;SetAlphaBitmap(&amp;bmpInfo);

        SelectObject(hdcBmp, hOld);
        DeleteDC(hdcBmp);
        ReleaseDC(m_hwndVideo, hdc);
    }
    else
    {
        hr = m_pMixerBitmap-&gt;ClearAlphaBitmap();
    }
    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/4da4bdb9-857b-40c9-b910-04a099a23ab5">IMFVideoMixerBitmap</a>
 

 

