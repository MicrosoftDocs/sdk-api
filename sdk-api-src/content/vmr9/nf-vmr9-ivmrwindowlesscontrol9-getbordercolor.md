---
UID: NF:vmr9.IVMRWindowlessControl9.GetBorderColor
title: IVMRWindowlessControl9::GetBorderColor (vmr9.h)
author: windows-sdk-content
description: The GetBorderColor method retrieves the current border color used by the VMR.
old-location: dshow\ivmrwindowlesscontrol9_getbordercolor.htm
tech.root: DirectShow
ms.assetid: 314e6977-fe6d-40b2-a566-0e894f3d881c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetBorderColor, GetBorderColor method [DirectShow], GetBorderColor method [DirectShow],IVMRWindowlessControl9 interface, IVMRWindowlessControl9 interface [DirectShow],GetBorderColor method, IVMRWindowlessControl9.GetBorderColor, IVMRWindowlessControl9::GetBorderColor, IVMRWindowlessControl9GetBorderColor, dshow.ivmrwindowlesscontrol9_getbordercolor, vmr9/IVMRWindowlessControl9::GetBorderColor
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
 - IVMRWindowlessControl9.GetBorderColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nn-vmr9-ivmrwindowlesscontrol9">IVMRWindowlessControl9 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-setbordercolor">SetBorderColor</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

