---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IVMRImageCompositor9::CompositeImage


## -description



The <code>CompositeImage</code> method composites the current frames available in each input stream.




## -parameters




### -param pD3DDevice [in]

Pointer to the <b>IUnknown</b> interface of the Direct3D device object.


### -param pddsRenderTarget [in]

Specifies the Direct3D surface that all drawing should be performed on.


### -param pmtRenderTarget [in]

Pointer to an <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure that contains the media type of the target surface.


### -param rtStart [in]

Specifies the start time.


### -param rtEnd [in]

Specifies the end time.


### -param dwClrBkGnd [in]

Specifies the background color, as a <b>D3DCOLOR</b> type.


### -param pVideoStreamInfo [in]

Pointer to an array of <a href="https://msdn.microsoft.com/e2da0c1e-d592-49ce-937c-0d75ce270282">VMR9VideoStreamInfo</a> structures, which descibe each video stream.


### -param cStreams [in]

Specifies the number of streams to mix, which is also the size of the <i>pVideoStreamInfo</i> array.


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
</table>
 




## -remarks



Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/19fda7f2-000f-47d0-a7c7-d8421de418a2">IVMRImageCompositor9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

