---
UID: NF:strmif.IVMRMixerBitmap.GetAlphaBitmapParameters
title: IVMRMixerBitmap::GetAlphaBitmapParameters (strmif.h)
description: The GetAlphaBitmapParameters method retrieves a copy of the current image and related blending parameters.
old-location: dshow\ivmrmixerbitmap_getalphabitmapparameters.htm
tech.root: DirectShow
ms.assetid: d03cc6ad-e09b-4af7-93b7-51880465c0b6
ms.date: 12/05/2018
ms.keywords: GetAlphaBitmapParameters, GetAlphaBitmapParameters method [DirectShow], GetAlphaBitmapParameters method [DirectShow],IVMRMixerBitmap interface, IVMRMixerBitmap interface [DirectShow],GetAlphaBitmapParameters method, IVMRMixerBitmap.GetAlphaBitmapParameters, IVMRMixerBitmap::GetAlphaBitmapParameters, IVMRMixerBitmapGetAlphaBitmapParameters, dshow.ivmrmixerbitmap_getalphabitmapparameters, strmif/IVMRMixerBitmap::GetAlphaBitmapParameters
f1_keywords:
- strmif/IVMRMixerBitmap.GetAlphaBitmapParameters
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRMixerBitmap::GetAlphaBitmapParameters


## -description



The <b>GetAlphaBitmapParameters</b> method retrieves a copy of the current image and related blending parameters.




## -parameters




### -param pBmpParms [out]

A pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ns-strmif-vmralphabitmap">VMRALPHABITMAP</a> structure that receives the bitmap, information about the blending values, and the location to blend it.
          


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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrmixerbitmap">IVMRMixerBitmap Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap">IVMRMixerBitmap::SetAlphaBitmap</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a>
 

 

