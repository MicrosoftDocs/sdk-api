---
UID: NF:vmr9.IVMRWindowlessControl9.SetBorderColor
title: IVMRWindowlessControl9::SetBorderColor
author: windows-sdk-content
description: The SetBorderColor method sets the border color to be used by the VMR.
old-location: dshow\ivmrwindowlesscontrol9_setbordercolor.htm
old-project: DirectShow
ms.assetid: 462b264d-1b4c-482a-b154-382748abaf92
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IVMRWindowlessControl9 interface [DirectShow],SetBorderColor method, IVMRWindowlessControl9.SetBorderColor, IVMRWindowlessControl9::SetBorderColor, IVMRWindowlessControl9SetBorderColor, SetBorderColor, SetBorderColor method [DirectShow], SetBorderColor method [DirectShow],IVMRWindowlessControl9 interface, dshow.ivmrwindowlesscontrol9_setbordercolor, vmr9/IVMRWindowlessControl9::SetBorderColor
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
 - IVMRWindowlessControl9.SetBorderColor
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRWindowlessControl9::SetBorderColor


## -description



The <code>SetBorderColor</code> method sets the border color to be used by the VMR.




## -parameters




### -param Clr [in]

Specifies the color as a <b>COLORREF</b> value.


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



The border color is used to fill any area of the destination rectangle that does not contain video. It is typically used in two situations:

<ul>
<li>When the video straddles two monitors</li>
<li>When the VMR is trying to maintain the aspect ratio of the movies by letter-boxing the video to fit within the specified destination rectangle. See <b>SetAspectRatioMode</b>.</li>
</ul>
Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/9db99c31-65b5-4ff1-9c0d-22140a3687e8">IVMRWindowlessControl9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

