---
UID: NF:strmif.IVMRWindowlessControl.GetBorderColor
title: IVMRWindowlessControl::GetBorderColor (strmif.h)
description: The GetBorderColor method retrieves the current border color used by the VMR.
helpviewer_keywords: ["GetBorderColor","GetBorderColor method [DirectShow]","GetBorderColor method [DirectShow]","IVMRWindowlessControl interface","IVMRWindowlessControl interface [DirectShow]","GetBorderColor method","IVMRWindowlessControl.GetBorderColor","IVMRWindowlessControl::GetBorderColor","IVMRWindowlessControlGetBorderColor","dshow.ivmrwindowlesscontrol_getbordercolor","strmif/IVMRWindowlessControl::GetBorderColor"]
old-location: dshow\ivmrwindowlesscontrol_getbordercolor.htm
tech.root: dshow
ms.assetid: f0bf04c8-17e6-4e1f-b35f-2e10c9de8b92
ms.date: 12/05/2018
ms.keywords: GetBorderColor, GetBorderColor method [DirectShow], GetBorderColor method [DirectShow],IVMRWindowlessControl interface, IVMRWindowlessControl interface [DirectShow],GetBorderColor method, IVMRWindowlessControl.GetBorderColor, IVMRWindowlessControl::GetBorderColor, IVMRWindowlessControlGetBorderColor, dshow.ivmrwindowlesscontrol_getbordercolor, strmif/IVMRWindowlessControl::GetBorderColor
f1_keywords:
- strmif/IVMRWindowlessControl.GetBorderColor
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
- IVMRWindowlessControl.GetBorderColor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRWindowlessControl::GetBorderColor


## -description



The <code>GetBorderColor</code> method retrieves the current border color used by the VMR.




## -parameters




### -param lpClr [out]

Pointer to a <b>COLORREF</b> variable that receives the current border color.


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
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The VMR is not in windowless mode.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrwindowlesscontrol">IVMRWindowlessControl Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrwindowlesscontrol-setbordercolor">IVMRWindowlessControl::SetBorderColor</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

