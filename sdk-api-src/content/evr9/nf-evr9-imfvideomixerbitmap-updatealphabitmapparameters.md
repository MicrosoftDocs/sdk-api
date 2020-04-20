---
UID: NF:evr9.IMFVideoMixerBitmap.UpdateAlphaBitmapParameters
title: IMFVideoMixerBitmap::UpdateAlphaBitmapParameters (evr9.h)
description: Updates the current alpha-blending settings, including the source and destination rectangles, the color key, and other information. You can update some or all of the blending parameters.helpviewer_keywords: ["369bf934-b0a0-44b2-bea2-e8575404d36d","IMFVideoMixerBitmap interface [Media Foundation]","UpdateAlphaBitmapParameters method","IMFVideoMixerBitmap.UpdateAlphaBitmapParameters","IMFVideoMixerBitmap::UpdateAlphaBitmapParameters","UpdateAlphaBitmapParameters","UpdateAlphaBitmapParameters method [Media Foundation]","UpdateAlphaBitmapParameters method [Media Foundation]","IMFVideoMixerBitmap interface","evr9/IMFVideoMixerBitmap::UpdateAlphaBitmapParameters","mf.imfvideomixerbitmap_updatealphabitmapparameters"]
old-location: mf\imfvideomixerbitmap_updatealphabitmapparameters.htm
tech.root: medfound
ms.assetid: 369bf934-b0a0-44b2-bea2-e8575404d36d
ms.date: 12/05/2018
ms.keywords: 369bf934-b0a0-44b2-bea2-e8575404d36d, IMFVideoMixerBitmap interface [Media Foundation],UpdateAlphaBitmapParameters method, IMFVideoMixerBitmap.UpdateAlphaBitmapParameters, IMFVideoMixerBitmap::UpdateAlphaBitmapParameters, UpdateAlphaBitmapParameters, UpdateAlphaBitmapParameters method [Media Foundation], UpdateAlphaBitmapParameters method [Media Foundation],IMFVideoMixerBitmap interface, evr9/IMFVideoMixerBitmap::UpdateAlphaBitmapParameters, mf.imfvideomixerbitmap_updatealphabitmapparameters
f1_keywords:
- evr9/IMFVideoMixerBitmap.UpdateAlphaBitmapParameters
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
api_name:
- IMFVideoMixerBitmap.UpdateAlphaBitmapParameters
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoMixerBitmap::UpdateAlphaBitmapParameters


## -description



Updates the current alpha-blending settings, including the source and destination rectangles, the color key, and other information. You can update some or all of the blending parameters.




## -parameters




### -param pBmpParms [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/evr9/ns-evr9-mfvideoalphabitmapparams">MFVideoAlphaBitmapParams</a> structure that contains the blending parameters.


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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
No bitmap is currently set. You must call <a href="https://docs.microsoft.com/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-setalphabitmap">IMFVideoMixerBitmap::SetAlphaBitmap</a> to set a bitmap.

</td>
</tr>
</table>
 




## -remarks



The video must be playing for the changes to take effect.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap">IMFVideoMixerBitmap</a>
 

 

