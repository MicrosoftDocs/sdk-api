---
UID: NF:vmr9.IVMRWindowlessControl9.GetCurrentImage
title: IVMRWindowlessControl9::GetCurrentImage
author: windows-sdk-content
description: The GetCurrentImage method retrieves a copy of the current image being displayed by the VMR.
old-location: dshow\ivmrwindowlesscontrol9_getcurrentimage.htm
tech.root: DirectShow
ms.assetid: dddba9a5-be25-4dc4-9d91-eaff78d2405d
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetCurrentImage, GetCurrentImage method [DirectShow], GetCurrentImage method [DirectShow],IVMRWindowlessControl9 interface, IVMRWindowlessControl9 interface [DirectShow],GetCurrentImage method, IVMRWindowlessControl9.GetCurrentImage, IVMRWindowlessControl9::GetCurrentImage, IVMRWindowlessControl9GetCurrentImage, dshow.ivmrwindowlesscontrol9_getcurrentimage, vmr9/IVMRWindowlessControl9::GetCurrentImage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IVMRWindowlessControl9.GetCurrentImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRWindowlessControl9::GetCurrentImage


## -description



The <code>GetCurrentImage</code> method retrieves a copy of the current image being displayed by the VMR.




## -parameters




### -param lpDib [out]

Address of a pointer to a BYTE that will receive the DIB.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The VMR is not in windowless mode.

</td>
</tr>
</table>
 




## -remarks



This method returns the current image being displayed. The image is returned in the form of packed Windows DIB. The image starts with a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure, possibly including palette entries and/or color masks, followed by the image data.

The VMR allocates the memory for the image and returns a pointer to it in the <i>lpDib</i> variable. The caller must free the memory by calling <b>CoTaskMemFree</b>.

This method can be called at any time, no matter what state the filter is in, whether running, stopped or paused. However, frequent calls to this method will degrade video playback performance.

Include DShow.h and D3d9.h before Vmr9.h.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
BYTE *lpDib = NULL;
hr = pWindowlessControl-&gt;GetCurrentImage(&amp;lpDib);
if (SUCCEEDED(hr))
{
    BITMAPINFOHEADER  *pBMIH = (BITMAPINFOHEADER*) lpDib;
    /* .... */
    CoTaskMemFree(lpDib);
}

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9db99c31-65b5-4ff1-9c0d-22140a3687e8">IVMRWindowlessControl9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

