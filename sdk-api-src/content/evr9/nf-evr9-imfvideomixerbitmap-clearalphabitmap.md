---
UID: NF:evr9.IMFVideoMixerBitmap.ClearAlphaBitmap
title: IMFVideoMixerBitmap::ClearAlphaBitmap
author: windows-sdk-content
description: Removes the current bitmap and releases any resources associated with it.
old-location: mf\imfvideomixerbitmap_clearalphabitmap.htm
tech.root: medfound
ms.assetid: 79a0f24c-9388-4c64-885f-5d04e671669e
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 79a0f24c-9388-4c64-885f-5d04e671669e, ClearAlphaBitmap, ClearAlphaBitmap method [Media Foundation], ClearAlphaBitmap method [Media Foundation],IMFVideoMixerBitmap interface, IMFVideoMixerBitmap interface [Media Foundation],ClearAlphaBitmap method, IMFVideoMixerBitmap.ClearAlphaBitmap, IMFVideoMixerBitmap::ClearAlphaBitmap, evr9/IMFVideoMixerBitmap::ClearAlphaBitmap, mf.imfvideomixerbitmap_clearalphabitmap
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
 - IMFVideoMixerBitmap.ClearAlphaBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoMixerBitmap::ClearAlphaBitmap


## -description



Removes the current bitmap and releases any resources associated with it.




## -parameters






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
No bitmap is currently set.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/4da4bdb9-857b-40c9-b910-04a099a23ab5">IMFVideoMixerBitmap</a>
 

 

