---
UID: NF:evr9.IMFVideoMixerBitmap.SetAlphaBitmap
title: IMFVideoMixerBitmap::SetAlphaBitmap (evr9.h)
description: Sets a bitmap image for the enhanced video renderer (EVR) to alpha-blend with the video.
helpviewer_keywords: ["IMFVideoMixerBitmap interface [Media Foundation]","SetAlphaBitmap method","IMFVideoMixerBitmap.SetAlphaBitmap","IMFVideoMixerBitmap::SetAlphaBitmap","SetAlphaBitmap","SetAlphaBitmap method [Media Foundation]","SetAlphaBitmap method [Media Foundation]","IMFVideoMixerBitmap interface","a70e6734-bf49-4dea-8bf6-917b8465cc78","evr9/IMFVideoMixerBitmap::SetAlphaBitmap","mf.imfvideomixerbitmap_setalphabitmap"]
old-location: mf\imfvideomixerbitmap_setalphabitmap.htm
tech.root: mfarchive
ms.assetid: a70e6734-bf49-4dea-8bf6-917b8465cc78
ms.date: 12/05/2018
ms.keywords: IMFVideoMixerBitmap interface [Media Foundation],SetAlphaBitmap method, IMFVideoMixerBitmap.SetAlphaBitmap, IMFVideoMixerBitmap::SetAlphaBitmap, SetAlphaBitmap, SetAlphaBitmap method [Media Foundation], SetAlphaBitmap method [Media Foundation],IMFVideoMixerBitmap interface, a70e6734-bf49-4dea-8bf6-917b8465cc78, evr9/IMFVideoMixerBitmap::SetAlphaBitmap, mf.imfvideomixerbitmap_setalphabitmap
req.header: evr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFVideoMixerBitmap::SetAlphaBitmap
 - evr9/IMFVideoMixerBitmap::SetAlphaBitmap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoMixerBitmap.SetAlphaBitmap
archived: true
---

# IMFVideoMixerBitmap::SetAlphaBitmap


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Sets a bitmap image for the enhanced video renderer (EVR) to alpha-blend with the video.

## -parameters

### -param pBmpParms [in]

Pointer to an <a href="/windows/desktop/api/evr9/ns-evr9-mfvideoalphabitmap">MFVideoAlphaBitmap</a> structure that contains information about the bitmap, the source and destination rectangles, the color key, and other information.

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


```
HRESULT EVRPlayer::SetBitmapImage(BOOL bEnable, HBITMAP hBitmap)
{
    const float fBitmapAlpha = 0.5f; 

    HRESULT hr = S_OK;

    // To enable the bitmap, you must supply a valid bitmap handle.
    if (bEnable && (hBitmap == NULL))
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

        // Create a compatible DC and select the bitmap into the DC>
        HDC hdcBmp = CreateCompatibleDC(hdc);
        HBITMAP hOld = (HBITMAP)SelectObject(hdcBmp, hBitmap);

        // Fill in the blending parameters.
        MFVideoAlphaBitmap bmpInfo;
        ZeroMemory(&bmpInfo, sizeof(bmpInfo));
        bmpInfo.GetBitmapFromDC = TRUE; // Use a bitmap DC (not a Direct3D surface).
        bmpInfo.bitmap.hdc = hdcBmp;
        bmpInfo.params.dwFlags = 
            MFVideoAlphaBitmap_Alpha | MFVideoAlphaBitmap_DestRect;
        bmpInfo.params.fAlpha = fBitmapAlpha;
        bmpInfo.params.nrcDest = nrcDest;

        // Get the bitmap dimensions.
        BITMAP bm;
        GetObject(hBitmap, sizeof(BITMAP), &bm);

        // Set the source rectangle equal to the entire bitmap.
        SetRect(&bmpInfo.params.rcSrc, 0, 0, bm.bmWidth, bm.bmHeight);

        // Set the bitmap.
        hr = m_pMixerBitmap->SetAlphaBitmap(&bmpInfo);

        SelectObject(hdcBmp, hOld);
        DeleteDC(hdcBmp);
        ReleaseDC(m_hwndVideo, hdc);
    }
    else
    {
        hr = m_pMixerBitmap->ClearAlphaBitmap();
    }
    return hr;
}
```

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap">IMFVideoMixerBitmap</a>