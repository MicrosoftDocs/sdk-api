---
UID: NF:vmr9.IVMRWindowlessControl9.SetVideoClippingWindow
title: IVMRWindowlessControl9::SetVideoClippingWindow
author: windows-sdk-content
description: The SetVideoClippingWindow method specifies the container window that video should be clipped to.
old-location: dshow\ivmrwindowlesscontrol9_setvideoclippingwindow.htm
tech.root: DirectShow
ms.assetid: 426476cd-a7e9-42ef-9d1b-5bbf921557ed
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IVMRWindowlessControl9 interface [DirectShow],SetVideoClippingWindow method, IVMRWindowlessControl9.SetVideoClippingWindow, IVMRWindowlessControl9::SetVideoClippingWindow, IVMRWindowlessControl9SetVideoClippingWindow, SetVideoClippingWindow, SetVideoClippingWindow method [DirectShow], SetVideoClippingWindow method [DirectShow],IVMRWindowlessControl9 interface, dshow.ivmrwindowlesscontrol9_setvideoclippingwindow, vmr9/IVMRWindowlessControl9::SetVideoClippingWindow
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
 - IVMRWindowlessControl9.SetVideoClippingWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRWindowlessControl9::SetVideoClippingWindow


## -description



The <code>SetVideoClippingWindow</code> method specifies the container window that video should be clipped to.




## -parameters




### -param hwnd [in]

Specifies the window to which the video should be clipped.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>hwnd</i> parameter is <b>NULL</b>.

</td>
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



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

