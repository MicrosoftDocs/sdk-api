---
UID: NF:strmif.IVMRWindowlessControl.SetBorderColor
title: IVMRWindowlessControl::SetBorderColor (strmif.h)
description: The SetBorderColor method sets the border color to be used by the VMR.
old-location: dshow\ivmrwindowlesscontrol_setbordercolor.htm
tech.root: DirectShow
ms.assetid: d58ce18f-ddc4-4d91-b086-8829056f4508
ms.date: 12/05/2018
ms.keywords: IVMRWindowlessControl interface [DirectShow],SetBorderColor method, IVMRWindowlessControl.SetBorderColor, IVMRWindowlessControl::SetBorderColor, IVMRWindowlessControlSetBorderColor, SetBorderColor, SetBorderColor method [DirectShow], SetBorderColor method [DirectShow],IVMRWindowlessControl interface, dshow.ivmrwindowlesscontrol_setbordercolor, strmif/IVMRWindowlessControl::SetBorderColor
ms.topic: method
f1_keywords:
- strmif/IVMRWindowlessControl.SetBorderColor
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
- IVMRWindowlessControl.SetBorderColor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRWindowlessControl::SetBorderColor


## -description



The <code>SetBorderColor</code> method sets the border color to be used by the VMR.




## -parameters




### -param Clr [in]

Specifies the border color.


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
 




## -remarks



The border color is color used to fill any area of the destination rectangle that does not contain video. It is typically used in two instances: (1) when the video straddles two monitors and (2) when the VMR is trying to maintain the aspect ratio of the movie by letter boxing the video to fit within the specified destination rectangle. See the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode">IVMRWindowlessControl::SetAspectRatioMode</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrwindowlesscontrol">IVMRWindowlessControl Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrwindowlesscontrol-getbordercolor">IVMRWindowlessControl::GetBorderColor</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

