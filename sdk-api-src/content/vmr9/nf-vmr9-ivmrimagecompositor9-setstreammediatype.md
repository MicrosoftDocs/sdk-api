---
UID: NF:vmr9.IVMRImageCompositor9.SetStreamMediaType
title: IVMRImageCompositor9::SetStreamMediaType
author: windows-sdk-content
description: The SetStreamMediaType method sets the media type for the input stream.
old-location: dshow\ivmrimagecompositor9_setstreammediatype.htm
old-project: DirectShow
ms.assetid: 4d994a83-a5be-427c-bf19-0090577d6ee5
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IVMRImageCompositor9 interface [DirectShow],SetStreamMediaType method, IVMRImageCompositor9.SetStreamMediaType, IVMRImageCompositor9::SetStreamMediaType, IVMRImageCompositor9SetStreamMediaType, SetStreamMediaType, SetStreamMediaType method [DirectShow], SetStreamMediaType method [DirectShow],IVMRImageCompositor9 interface, dshow.ivmrimagecompositor9_setstreammediatype, vmr9/IVMRImageCompositor9::SetStreamMediaType
ms.prod: windows
ms.technology: windows-sdk
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
 - IVMRImageCompositor9.SetStreamMediaType
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRImageCompositor9::SetStreamMediaType


## -description



The <code>SetStreamMediaType</code> method sets the media type for the input stream.




## -parameters




### -param dwStrmID [in]

Specifies the input stream; must be from 1 through 16.


### -param pmt [in]

Pointer to the AM_MEDIA_TYPE struct that specifies the media type.


### -param fTexture [in]

If <b>TRUE</b>, specifies that the target surface is a Direct3D texture surface.


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
 

 

