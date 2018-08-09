---
UID: NF:evr.IMFVideoDisplayControl.GetCurrentImage
title: IMFVideoDisplayControl::GetCurrentImage
author: windows-sdk-content
description: Gets a copy of the current image being displayed by the video renderer.
old-location: mf\imfvideodisplaycontrol_getcurrentimage.htm
old-project: medfound
ms.assetid: 25ec4c23-04dd-4e18-9cc1-de9e57271e8f
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 25ec4c23-04dd-4e18-9cc1-de9e57271e8f, GetCurrentImage, GetCurrentImage method [Media Foundation], GetCurrentImage method [Media Foundation],IMFVideoDisplayControl interface, IMFVideoDisplayControl interface [Media Foundation],GetCurrentImage method, IMFVideoDisplayControl.GetCurrentImage, IMFVideoDisplayControl::GetCurrentImage, evr/IMFVideoDisplayControl::GetCurrentImage, mf.imfvideodisplaycontrol_getcurrentimage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MFVideoMixPrefs
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
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFVideoDisplayControl::GetCurrentImage


## -description


Gets a copy of the current image being displayed by the video renderer.
        


## -parameters




### -param pBih [in, out]

Pointer to a <b>BITMAPINFOHEADER</b> structure that receives a description of the bitmap. Set the <b>biSize</b> member of the structure to <code>sizeof(BITMAPINFOHEADER)</code> before calling the method.


### -param pDib [out]

Receives a pointer to a buffer that contains a packed Windows device-independent bitmap (DIB). The caller must free the memory for the bitmap by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


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

In windowed mode, the bitmap is the size of the destination rectangle specified in <a href="https://msdn.microsoft.com/5dc789b7-e206-4f1d-a0b2-12cb98ce4184">IMFVideoDisplayControl::SetVideoPosition</a>. In full-screen mode, the bitmap is the size of the display.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/db9b4663-9240-484f-8c47-cb1f5daa238d">IMFVideoDisplayControl</a>



<a href="https://msdn.microsoft.com/09501d67-effb-41ce-a7b7-d2415acdf3ac">Using the Video Display Controls</a>
 

 

