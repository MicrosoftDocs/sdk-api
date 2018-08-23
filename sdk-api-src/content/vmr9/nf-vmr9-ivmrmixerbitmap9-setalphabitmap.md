---
UID: NF:vmr9.IVMRMixerBitmap9.SetAlphaBitmap
title: IVMRMixerBitmap9::SetAlphaBitmap
author: windows-sdk-content
description: The SetAlphaBitmap method specifies a new bitmap image and the source location of the bitmap and how and where it should be rendered on the destination rectangle.
old-location: dshow\ivmrmixerbitmap9_setalphabitmap.htm
old-project: DirectShow
ms.assetid: 22aadb5b-8dc8-48ec-bff1-1bac498f3984
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IVMRMixerBitmap9 interface [DirectShow],SetAlphaBitmap method, IVMRMixerBitmap9.SetAlphaBitmap, IVMRMixerBitmap9::SetAlphaBitmap, IVMRMixerBitmap9SetAlphaBitmap, SetAlphaBitmap, SetAlphaBitmap method [DirectShow], SetAlphaBitmap method [DirectShow],IVMRMixerBitmap9 interface, dshow.ivmrmixerbitmap9_setalphabitmap, vmr9/IVMRMixerBitmap9::SetAlphaBitmap
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vmr9.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VMR9DeinterlaceTech
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRMixerBitmap9.SetAlphaBitmap
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRMixerBitmap9::SetAlphaBitmap


## -description



The <code>SetAlphaBitmap</code> method specifies a new bitmap image and the source location of the bitmap and how and where it should be rendered on the destination rectangle.




## -parameters




### -param pBmpParms [in]

Pointer to a <a href="https://msdn.microsoft.com/62214c24-0a4b-43c3-91dc-3eb6e5df3d94">VMR9AlphaBitmap</a> structure that contains information about the bitmap.


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



To remove the bitmap, set the VMR9AlphaBitmap_Disable flag in the <b>VMR9AlphaBitmap</b> structure and call <code>SetAlphaBitmap</code> again.

The application can provide the bitmap either as a Direct3D surface or as a GDI bitmap. To use a Direct3D surface, set the <b>pDDS</b> member of the <a href="https://msdn.microsoft.com/62214c24-0a4b-43c3-91dc-3eb6e5df3d94">VMR9AlphaBitmap</a> structure. To use a GDI bitmap, set the <b>hdc</b> member of the structure.

The bitmap is mixed onto the video frame by the VMR's mixer component. The mixer draws the bitmap once per frame. If you change the bitmap while the filter graph is paused or stopped, the mixer does not use the new bitmap until the graph restarts. You can work around this limitation by calling <a href="https://msdn.microsoft.com/55dd55b1-51f0-4b47-8432-99741eaee8bb">IMediaControl::StopWhenReady</a>, although a better solution is to write a custom allocator-presenter to draw the bitmap. For more information, see <a href="https://msdn.microsoft.com/61bb6b0d-25b5-481b-a241-74c6e421f109">Supplying a Custom Allocator-Presenter for VMR-9</a>.

If the method returns E_INVALIDARG, possible reasons include the following:

<ul>
<li>The Direct3D surface was not allocated from the D3DPOOL_SYSTEMMEM pool.</li>
<li>Invalid surface format. If a Direct3D surface is used, the surface format must be D3DFMT_X8R8G8B8 or D3DFMT_A8R8G8B8. If the surface format is D3DFMT_A8R8G8B8, the VMR9AlphaBitmap_SrcColorKey flag cannot be used.</li>
<li>The source rectangle (rSrc) exceeds the boundaries of the Direct3D surface.</li>
<li>The source rectangle is empty.</li>
<li>The source rectangle exceeds the maximum texture width or maximum texture height for the Direct3D device. To find the maximum texture size, call <b>IDirect3DDevice9::GetDeviceCaps</b>.</li>
<li>The <b>dwFilterMode</b> member contains an invalid combination of flags.</li>
</ul>
Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/a5e5891f-6842-40e7-8bf4-29c6979c7551">GetAlphaBitmapParameters</a>



<a href="https://msdn.microsoft.com/de48307a-3522-49a0-b0a5-73ce7cf90517">IVMRMixerBitmap9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

