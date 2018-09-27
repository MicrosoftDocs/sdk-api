---
UID: NF:strmif.IVMRWindowlessControl.SetVideoClippingWindow
title: IVMRWindowlessControl::SetVideoClippingWindow
author: windows-sdk-content
description: The SetVideoClippingWindow method specifies the container window that video should be clipped to.
old-location: dshow\ivmrwindowlesscontrol_setvideoclippingwindow.htm
tech.root: DirectShow
ms.assetid: 82589745-8f79-4e0e-b28c-5a395390ba64
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVMRWindowlessControl interface [DirectShow],SetVideoClippingWindow method, IVMRWindowlessControl.SetVideoClippingWindow, IVMRWindowlessControl::SetVideoClippingWindow, IVMRWindowlessControlSetVideoClippingWindow, SetVideoClippingWindow, SetVideoClippingWindow method [DirectShow], SetVideoClippingWindow method [DirectShow],IVMRWindowlessControl interface, dshow.ivmrwindowlesscontrol_setvideoclippingwindow, strmif/IVMRWindowlessControl::SetVideoClippingWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c21c5611-f376-4899-9914-c14a18af3810">IVMRWindowlessControl Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

