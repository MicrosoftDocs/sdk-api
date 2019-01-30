---
UID: NF:strmif.IVMRWindowlessControl.GetBorderColor
title: IVMRWindowlessControl::GetBorderColor
author: windows-sdk-content
description: The GetBorderColor method retrieves the current border color used by the VMR.
old-location: dshow\ivmrwindowlesscontrol_getbordercolor.htm
tech.root: DirectShow
ms.assetid: f0bf04c8-17e6-4e1f-b35f-2e10c9de8b92
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetBorderColor, GetBorderColor method [DirectShow], GetBorderColor method [DirectShow],IVMRWindowlessControl interface, IVMRWindowlessControl interface [DirectShow],GetBorderColor method, IVMRWindowlessControl.GetBorderColor, IVMRWindowlessControl::GetBorderColor, IVMRWindowlessControlGetBorderColor, dshow.ivmrwindowlesscontrol_getbordercolor, strmif/IVMRWindowlessControl::GetBorderColor
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
 - IVMRWindowlessControl.GetBorderColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c21c5611-f376-4899-9914-c14a18af3810">IVMRWindowlessControl Interface</a>



<a href="https://msdn.microsoft.com/d58ce18f-ddc4-4d91-b086-8829056f4508">IVMRWindowlessControl::SetBorderColor</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

