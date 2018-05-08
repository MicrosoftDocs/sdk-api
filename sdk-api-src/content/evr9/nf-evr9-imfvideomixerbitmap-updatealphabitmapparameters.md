---
UID: NF:evr9.IMFVideoMixerBitmap.UpdateAlphaBitmapParameters
title: IMFVideoMixerBitmap::UpdateAlphaBitmapParameters
author: windows-driver-content
description: Updates the current alpha-blending settings, including the source and destination rectangles, the color key, and other information. You can update some or all of the blending parameters.
old-location: mf\imfvideomixerbitmap_updatealphabitmapparameters.htm
old-project: medfound
ms.assetid: 369bf934-b0a0-44b2-bea2-e8575404d36d
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: 369bf934-b0a0-44b2-bea2-e8575404d36d, IMFVideoMixerBitmap interface [Media Foundation],UpdateAlphaBitmapParameters method, IMFVideoMixerBitmap.UpdateAlphaBitmapParameters, IMFVideoMixerBitmap::UpdateAlphaBitmapParameters, UpdateAlphaBitmapParameters, UpdateAlphaBitmapParameters method [Media Foundation], UpdateAlphaBitmapParameters method [Media Foundation],IMFVideoMixerBitmap interface, evr9/IMFVideoMixerBitmap::UpdateAlphaBitmapParameters, mf.imfvideomixerbitmap_updatealphabitmapparameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: MFVideoAlphaBitmapFlags
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	strmiids.lib
-	strmiids.dll
api_name:
-	IMFVideoMixerBitmap.UpdateAlphaBitmapParameters
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFVideoMixerBitmap::UpdateAlphaBitmapParameters


## -description



Updates the current alpha-blending settings, including the source and destination rectangles, the color key, and other information. You can update some or all of the blending parameters.




## -parameters




### -param pBmpParms [in]

Pointer to an <a href="https://msdn.microsoft.com/3a7f67fa-ca54-4b6f-9cfc-e8eba57f00ce">MFVideoAlphaBitmapParams</a> structure that contains the blending parameters.


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
No bitmap is currently set. You must call <a href="https://msdn.microsoft.com/a70e6734-bf49-4dea-8bf6-917b8465cc78">IMFVideoMixerBitmap::SetAlphaBitmap</a> to set a bitmap.

</td>
</tr>
</table>
 




## -remarks



The video must be playing for the changes to take effect.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/4da4bdb9-857b-40c9-b910-04a099a23ab5">IMFVideoMixerBitmap</a>
 

 

