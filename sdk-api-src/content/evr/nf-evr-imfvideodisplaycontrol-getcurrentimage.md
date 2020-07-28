---
UID: NF:evr.IMFVideoDisplayControl.GetCurrentImage
title: IMFVideoDisplayControl::GetCurrentImage (evr.h)
description: Gets a copy of the current image being displayed by the video renderer.
helpviewer_keywords: ["25ec4c23-04dd-4e18-9cc1-de9e57271e8f","GetCurrentImage","GetCurrentImage method [Media Foundation]","GetCurrentImage method [Media Foundation]","IMFVideoDisplayControl interface","IMFVideoDisplayControl interface [Media Foundation]","GetCurrentImage method","IMFVideoDisplayControl.GetCurrentImage","IMFVideoDisplayControl::GetCurrentImage","evr/IMFVideoDisplayControl::GetCurrentImage","mf.imfvideodisplaycontrol_getcurrentimage"]
old-location: mf\imfvideodisplaycontrol_getcurrentimage.htm
tech.root: mf
ms.assetid: 25ec4c23-04dd-4e18-9cc1-de9e57271e8f
ms.date: 12/05/2018
ms.keywords: 25ec4c23-04dd-4e18-9cc1-de9e57271e8f, GetCurrentImage, GetCurrentImage method [Media Foundation], GetCurrentImage method [Media Foundation],IMFVideoDisplayControl interface, IMFVideoDisplayControl interface [Media Foundation],GetCurrentImage method, IMFVideoDisplayControl.GetCurrentImage, IMFVideoDisplayControl::GetCurrentImage, evr/IMFVideoDisplayControl::GetCurrentImage, mf.imfvideodisplaycontrol_getcurrentimage
f1_keywords:
- evr/IMFVideoDisplayControl.GetCurrentImage
dev_langs:
- c++
req.header: evr.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
api_name:
- IMFVideoDisplayControl.GetCurrentImage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoDisplayControl::GetCurrentImage


## -description


Gets a copy of the current image being displayed by the video renderer.
        


## -parameters




### -param pBih [in, out]

Pointer to a <b>BITMAPINFOHEADER</b> structure that receives a description of the bitmap. Set the <b>biSize</b> member of the structure to <code>sizeof(BITMAPINFOHEADER)</code> before calling the method.


### -param pDib [out]

Receives a pointer to a buffer that contains a packed Windows device-independent bitmap (DIB). The caller must free the memory for the bitmap by calling <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.


### -param pcbDib [out]

Receives the size of the buffer returned in <i>pDib</i>, in bytes.


### -param pTimeStamp [in, out]

Receives the time stamp of the captured image.


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
<dt><b>MF_E_LICENSE_INCORRECT_RIGHTS</b></dt>
</dl>
</td>
<td width="60%">
The content is protected and the license does not permit capturing the image.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The video renderer has been shut down.

</td>
</tr>
</table>
 




## -remarks



This method can be called at any time. However, calling the method too frequently degrades the video playback performance.

This method retrieves a copy of the final composited image, which includes any substreams, alpha-blended bitmap, aspect ratio correction, background color, and so forth.

In windowed mode, the bitmap is the size of the destination rectangle specified in <a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition">IMFVideoDisplayControl::SetVideoPosition</a>. In full-screen mode, the bitmap is the size of the display.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol">IMFVideoDisplayControl</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-the-video-display-controls">Using the Video Display Controls</a>
 

 

