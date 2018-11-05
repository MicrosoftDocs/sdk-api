---
UID: NF:strmif.IVMRWindowlessControl.GetCurrentImage
title: IVMRWindowlessControl::GetCurrentImage
author: windows-sdk-content
description: The GetCurrentImage method retrieves a copy of the current image being displayed by the VMR.
old-location: dshow\ivmrwindowlesscontrol_getcurrentimage.htm
tech.root: DirectShow
ms.assetid: 515e252d-4ac4-49ec-8d94-bf850dd4783f
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetCurrentImage, GetCurrentImage method [DirectShow], GetCurrentImage method [DirectShow],IVMRWindowlessControl interface, IVMRWindowlessControl interface [DirectShow],GetCurrentImage method, IVMRWindowlessControl.GetCurrentImage, IVMRWindowlessControl::GetCurrentImage, IVMRWindowlessControlGetCurrentImage, dshow.ivmrwindowlesscontrol_getcurrentimage, strmif/IVMRWindowlessControl::GetCurrentImage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRWindowlessControl.GetCurrentImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRWindowlessControl::GetCurrentImage


## -description



The <code>GetCurrentImage</code> method retrieves a copy of the current image being displayed by the VMR.




## -parameters




### -param lpDib [out]

Address of a pointer to a BYTE array.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The VMR is not in windowless mode.

</td>
</tr>
</table>
 




## -remarks



This method returns the current image being displayed. The image is returned in the form of packed Windows DIB. The image starts with a <b>BITMAPINFOHEADER</b> structure, possibly including palette entries and/or color masks, followed by the image data.

The VMR allocates the memory for the image and returns a pointer to it in the <i>lpDib</i> variable. The caller must free the memory by calling <b>CoTaskMemFree</b>.

This method can be called at any time, no matter what state the filter is in, whether running, stopped or paused. However, frequent calls to this method will degrade video playback performance.


#### Examples


```cpp

BYTE *lpDib = NULL;
hr = pWindowlessControl->GetCurrentImage(&lpDib);
if (SUCCEEDED(hr))
{
    BITMAPINFOHEADER *pBMIH = (BITMAPINFOHEADER*)lpDib;
    /* .... */
    CoTaskMemFree(lpDib);
}
```





## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c21c5611-f376-4899-9914-c14a18af3810">IVMRWindowlessControl Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

