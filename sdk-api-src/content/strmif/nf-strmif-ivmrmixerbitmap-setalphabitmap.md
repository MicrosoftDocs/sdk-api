---
UID: NF:strmif.IVMRMixerBitmap.SetAlphaBitmap
title: IVMRMixerBitmap::SetAlphaBitmap
author: windows-sdk-content
description: The SetAlphaBitmap method specifies a new bitmap image and the source location of the bitmap and how and where it should be rendered on the destination rectangle.
old-location: dshow\ivmrmixerbitmap_setalphabitmap.htm
tech.root: DirectShow
ms.assetid: 92e57c3a-6761-4a54-83f5-0ea0ce80d60b
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IVMRMixerBitmap interface [DirectShow],SetAlphaBitmap method, IVMRMixerBitmap.SetAlphaBitmap, IVMRMixerBitmap::SetAlphaBitmap, IVMRMixerBitmapSetAlphaBitmap, SetAlphaBitmap, SetAlphaBitmap method [DirectShow], SetAlphaBitmap method [DirectShow],IVMRMixerBitmap interface, dshow.ivmrmixerbitmap_setalphabitmap, strmif/IVMRMixerBitmap::SetAlphaBitmap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IVMRMixerBitmap.SetAlphaBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRMixerBitmap::SetAlphaBitmap


## -description



The <b>SetAlphaBitmap</b> method specifies a new bitmap image and the source location of the bitmap and how and where it should be rendered on the destination rectangle.




## -parameters




### -param pBmpParms [in]

A oointer to a <a href="https://msdn.microsoft.com/03b3e619-4804-42de-88d5-5422089e875a">VMRALPHABITMAP</a> structure that contains information about the bitmap.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pBmpParms</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument. See Remarks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Could not create a destination DC or DIBSection for the bitmap.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
BitBlt to bitmap surface failed.

</td>
</tr>
</table>
 




## -remarks



To remove the bitmap, set the <b>VMRBITMAP_DISABLE</b> flag in the <a href="https://msdn.microsoft.com/03b3e619-4804-42de-88d5-5422089e875a">VMRALPHABITMAP</a> structure and call <b>SetAlphaBitmap</b> again.

The method might return <b>E_INVALIDARG</b> for several reasons:

<ul>
<li>The <b>dwFlags</b> member of the <a href="https://msdn.microsoft.com/03b3e619-4804-42de-88d5-5422089e875a">VMRALPHABITMAP</a> structure contains an invalid combination of flags.</li>
<li>The <a href="https://msdn.microsoft.com/03b3e619-4804-42de-88d5-5422089e875a">VMRALPHABITMAP</a> structure does not specify a valid HDC or DirectDraw surface.</li>
<li>The value of <b>fAlpha</b> is invalid.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ac7da3f9-2c17-4517-bb64-6b56257a65c3">IVMRMixerBitmap Interface</a>



<a href="https://msdn.microsoft.com/d03cc6ad-e09b-4af7-93b7-51880465c0b6">IVMRMixerBitmap::GetAlphaBitmapParameters</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>



<a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a>
 

 

