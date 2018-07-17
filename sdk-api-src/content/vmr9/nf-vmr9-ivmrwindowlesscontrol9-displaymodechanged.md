---
UID: NF:vmr9.IVMRWindowlessControl9.DisplayModeChanged
title: IVMRWindowlessControl9::DisplayModeChanged
author: windows-sdk-content
description: The DisplayModeChanged method informs the VMR that a WM_DISPLAYCHANGE message has been received by the application.
old-location: dshow\ivmrwindowlesscontrol9_displaymodechanged.htm
old-project: DirectShow
ms.assetid: ad023fa0-3540-4009-abdc-a1c980f906ec
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: DisplayModeChanged, DisplayModeChanged method [DirectShow], DisplayModeChanged method [DirectShow],IVMRWindowlessControl9 interface, IVMRWindowlessControl9 interface [DirectShow],DisplayModeChanged method, IVMRWindowlessControl9.DisplayModeChanged, IVMRWindowlessControl9::DisplayModeChanged, IVMRWindowlessControl9DisplayModeChanged, dshow.ivmrwindowlesscontrol9_displaymodechanged, vmr9/IVMRWindowlessControl9::DisplayModeChanged
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
 - IVMRWindowlessControl9.DisplayModeChanged
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRWindowlessControl9::DisplayModeChanged


## -description



The <code>DisplayModeChanged</code> method informs the VMR that a WM_DISPLAYCHANGE message has been received by the application.




## -parameters






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



An application must call this method whenever it receives a WM_DISPLAYCHANGE window message, but only if the VMR is currently in windowless mode.

Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/9db99c31-65b5-4ff1-9c0d-22140a3687e8">IVMRWindowlessControl9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

