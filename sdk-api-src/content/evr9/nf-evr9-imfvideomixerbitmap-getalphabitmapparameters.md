---
UID: NF:evr9.IMFVideoMixerBitmap.GetAlphaBitmapParameters
title: IMFVideoMixerBitmap::GetAlphaBitmapParameters
author: windows-sdk-content
description: Retrieves the current settings that the enhanced video renderer (EVR) uses to alpha-blend the bitmap with the video.
old-location: mf\imfvideomixerbitmap_getalphabitmapparameters.htm
tech.root: medfound
ms.assetid: 0361e340-9de7-47f3-80fd-61d5e914d44e
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 0361e340-9de7-47f3-80fd-61d5e914d44e, GetAlphaBitmapParameters, GetAlphaBitmapParameters method [Media Foundation], GetAlphaBitmapParameters method [Media Foundation],IMFVideoMixerBitmap interface, IMFVideoMixerBitmap interface [Media Foundation],GetAlphaBitmapParameters method, IMFVideoMixerBitmap.GetAlphaBitmapParameters, IMFVideoMixerBitmap::GetAlphaBitmapParameters, evr9/IMFVideoMixerBitmap::GetAlphaBitmapParameters, mf.imfvideomixerbitmap_getalphabitmapparameters
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
 - IMFVideoMixerBitmap.GetAlphaBitmapParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoMixerBitmap::GetAlphaBitmapParameters


## -description



Retrieves the current settings that the enhanced video renderer (EVR) uses to alpha-blend the bitmap with the video.




## -parameters




### -param pBmpParms [out]

Pointer to an <a href="https://msdn.microsoft.com/3a7f67fa-ca54-4b6f-9cfc-e8eba57f00ce">MFVideoAlphaBitmapParams</a> structure that receives the current blending parameters.


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
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
No bitmap is currently set. You must call <a href="https://msdn.microsoft.com/a70e6734-bf49-4dea-8bf6-917b8465cc78">IMFVideoMixerBitmap::SetAlphaBitmap</a> to set a bitmap.

</td>
</tr>
</table>
 




## -remarks



This method returns the current values of all the blending parameters, not just those that the application specified. Ignore the <b>dwFlags</b> member of the structure.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/4da4bdb9-857b-40c9-b910-04a099a23ab5">IMFVideoMixerBitmap</a>
 

 

