---
UID: NF:strmif.IVMRWindowlessControl.DisplayModeChanged
title: IVMRWindowlessControl::DisplayModeChanged
author: windows-sdk-content
description: The DisplayModeChanged method informs the VMR that a WM_DISPLAYCHANGE message has been received by the application.
old-location: dshow\ivmrwindowlesscontrol_displaymodechanged.htm
old-project: DirectShow
ms.assetid: 83fbca03-0e8c-4386-96ff-f572f0b13312
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: DisplayModeChanged, DisplayModeChanged method [DirectShow], DisplayModeChanged method [DirectShow],IVMRWindowlessControl interface, IVMRWindowlessControl interface [DirectShow],DisplayModeChanged method, IVMRWindowlessControl.DisplayModeChanged, IVMRWindowlessControl::DisplayModeChanged, IVMRWindowlessControlDisplayModeChanged, dshow.ivmrwindowlesscontrol_displaymodechanged, strmif/IVMRWindowlessControl::DisplayModeChanged
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRWindowlessControl.DisplayModeChanged
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRWindowlessControl::DisplayModeChanged


## -description



The <code>DisplayModeChanged</code> method informs the VMR that a WM_DISPLAYCHANGE message has been received by the application.




## -parameters






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



An application must call this method whenever it receives a WM_DISPLAYCHANGE window message, but only if the VMR is currently in windowless mode.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c21c5611-f376-4899-9914-c14a18af3810">IVMRWindowlessControl Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

