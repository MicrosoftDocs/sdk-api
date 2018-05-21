---
UID: NF:vmr9.IVMRWindowlessControl9.GetBorderColor
title: IVMRWindowlessControl9::GetBorderColor
author: windows-driver-content
description: The GetBorderColor method retrieves the current border color used by the VMR.
old-location: dshow\ivmrwindowlesscontrol9_getbordercolor.htm
old-project: DirectShow
ms.assetid: 314e6977-fe6d-40b2-a566-0e894f3d881c
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetBorderColor, GetBorderColor method [DirectShow], GetBorderColor method [DirectShow],IVMRWindowlessControl9 interface, IVMRWindowlessControl9 interface [DirectShow],GetBorderColor method, IVMRWindowlessControl9.GetBorderColor, IVMRWindowlessControl9::GetBorderColor, IVMRWindowlessControl9GetBorderColor, dshow.ivmrwindowlesscontrol9_getbordercolor, vmr9/IVMRWindowlessControl9::GetBorderColor
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
req.typenames: VMR9DeinterlaceTech
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVMRWindowlessControl9.GetBorderColor
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRWindowlessControl9::GetBorderColor


## -description



The <code>GetBorderColor</code> method retrieves the current border color used by the VMR.




## -parameters




### -param lpClr [out]

Pointer to a <b>COLORREF</b> variable that receives the current border color.


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
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The VMR is not in windowless mode.

</td>
</tr>
</table>
 




## -remarks



Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/9db99c31-65b5-4ff1-9c0d-22140a3687e8">IVMRWindowlessControl9 Interface</a>



<a href="https://msdn.microsoft.com/462b264d-1b4c-482a-b154-382748abaf92">SetBorderColor</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

