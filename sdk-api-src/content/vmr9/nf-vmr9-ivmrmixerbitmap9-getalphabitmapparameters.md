---
UID: NF:vmr9.IVMRMixerBitmap9.GetAlphaBitmapParameters
title: IVMRMixerBitmap9::GetAlphaBitmapParameters
author: windows-sdk-content
description: The GetAlphaBitmapParameters method retrieves a copy of the current image and related blending parameters.
old-location: dshow\ivmrmixerbitmap9_getalphabitmapparameters.htm
tech.root: DirectShow
ms.assetid: a5e5891f-6842-40e7-8bf4-29c6979c7551
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetAlphaBitmapParameters, GetAlphaBitmapParameters method [DirectShow], GetAlphaBitmapParameters method [DirectShow],IVMRMixerBitmap9 interface, IVMRMixerBitmap9 interface [DirectShow],GetAlphaBitmapParameters method, IVMRMixerBitmap9.GetAlphaBitmapParameters, IVMRMixerBitmap9::GetAlphaBitmapParameters, IVMRMixerBitmap9GetAlphaBitmapParameters, dshow.ivmrmixerbitmap9_getalphabitmapparameters, vmr9/IVMRMixerBitmap9::GetAlphaBitmapParameters
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
 - IVMRMixerBitmap9.GetAlphaBitmapParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRMixerBitmap9::GetAlphaBitmapParameters


## -description



The <code>GetAlphaBitmapParameters</code> method retrieves a copy of the current image and related blending parameters.




## -parameters




### -param pBmpParms [out]

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dd407359(v=VS.85).aspx">VMR9AlphaBitmap</a> structure that receives the bitmap, information about the blending values, and the location to blend it.


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
<i>pBmpParms</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The mixer has not been loaded.

</td>
</tr>
</table>
 




## -remarks



Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd390449(v=VS.85).aspx">IVMRMixerBitmap9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

