---
UID: NF:strmif.IVMRWindowlessControl.SetVideoClippingWindow
title: IVMRWindowlessControl::SetVideoClippingWindow (strmif.h)
description: The SetVideoClippingWindow method specifies the container window that video should be clipped to.
helpviewer_keywords: ["IVMRWindowlessControl interface [DirectShow]","SetVideoClippingWindow method","IVMRWindowlessControl.SetVideoClippingWindow","IVMRWindowlessControl::SetVideoClippingWindow","IVMRWindowlessControlSetVideoClippingWindow","SetVideoClippingWindow","SetVideoClippingWindow method [DirectShow]","SetVideoClippingWindow method [DirectShow]","IVMRWindowlessControl interface","dshow.ivmrwindowlesscontrol_setvideoclippingwindow","strmif/IVMRWindowlessControl::SetVideoClippingWindow"]
old-location: dshow\ivmrwindowlesscontrol_setvideoclippingwindow.htm
tech.root: DirectShow
ms.assetid: 82589745-8f79-4e0e-b28c-5a395390ba64
ms.date: 12/05/2018
ms.keywords: IVMRWindowlessControl interface [DirectShow],SetVideoClippingWindow method, IVMRWindowlessControl.SetVideoClippingWindow, IVMRWindowlessControl::SetVideoClippingWindow, IVMRWindowlessControlSetVideoClippingWindow, SetVideoClippingWindow, SetVideoClippingWindow method [DirectShow], SetVideoClippingWindow method [DirectShow],IVMRWindowlessControl interface, dshow.ivmrwindowlesscontrol_setvideoclippingwindow, strmif/IVMRWindowlessControl::SetVideoClippingWindow
f1_keywords:
- strmif/IVMRWindowlessControl.SetVideoClippingWindow
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
- IVMRWindowlessControl.SetVideoClippingWindow
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRWindowlessControl::SetVideoClippingWindow


## -description



The <code>SetVideoClippingWindow</code> method specifies the container window that video should be clipped to.




## -parameters




### -param hwnd [in]

Specifies the window to which the video should be clipped.


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



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

