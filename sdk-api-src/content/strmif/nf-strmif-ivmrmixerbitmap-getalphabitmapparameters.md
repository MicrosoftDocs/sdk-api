---
UID: NF:strmif.IVMRMixerBitmap.GetAlphaBitmapParameters
title: IVMRMixerBitmap::GetAlphaBitmapParameters
author: windows-sdk-content
description: The GetAlphaBitmapParameters method retrieves a copy of the current image and related blending parameters.
old-location: dshow\ivmrmixerbitmap_getalphabitmapparameters.htm
tech.root: DirectShow
ms.assetid: d03cc6ad-e09b-4af7-93b7-51880465c0b6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetAlphaBitmapParameters, GetAlphaBitmapParameters method [DirectShow], GetAlphaBitmapParameters method [DirectShow],IVMRMixerBitmap interface, IVMRMixerBitmap interface [DirectShow],GetAlphaBitmapParameters method, IVMRMixerBitmap.GetAlphaBitmapParameters, IVMRMixerBitmap::GetAlphaBitmapParameters, IVMRMixerBitmapGetAlphaBitmapParameters, dshow.ivmrmixerbitmap_getalphabitmapparameters, strmif/IVMRMixerBitmap::GetAlphaBitmapParameters
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
 - IVMRMixerBitmap.GetAlphaBitmapParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IVMRMixerBitmap.GetAlphaBitmapParameters
: 
---

# IVMRMixerBitmap::GetAlphaBitmapParameters


## -description



The <b>GetAlphaBitmapParameters</b> method retrieves a copy of the current image and related blending parameters.




## -parameters




### -param pBmpParms [out]

A pointer to a <a href="https://msdn.microsoft.com/03b3e619-4804-42de-88d5-5422089e875a">VMRALPHABITMAP</a> structure that receives the bitmap, information about the blending values, and the location to blend it.
          


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
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ac7da3f9-2c17-4517-bb64-6b56257a65c3">IVMRMixerBitmap Interface</a>



<a href="https://msdn.microsoft.com/92e57c3a-6761-4a54-83f5-0ea0ce80d60b">IVMRMixerBitmap::SetAlphaBitmap</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>



<a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a>
 

 

