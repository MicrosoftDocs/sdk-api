---
UID: NF:strmif.IVMRWindowlessControl.SetBorderColor
title: IVMRWindowlessControl::SetBorderColor
author: windows-sdk-content
description: The SetBorderColor method sets the border color to be used by the VMR.
old-location: dshow\ivmrwindowlesscontrol_setbordercolor.htm
tech.root: DirectShow
ms.assetid: d58ce18f-ddc4-4d91-b086-8829056f4508
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IVMRWindowlessControl interface [DirectShow],SetBorderColor method, IVMRWindowlessControl.SetBorderColor, IVMRWindowlessControl::SetBorderColor, IVMRWindowlessControlSetBorderColor, SetBorderColor, SetBorderColor method [DirectShow], SetBorderColor method [DirectShow],IVMRWindowlessControl interface, dshow.ivmrwindowlesscontrol_setbordercolor, strmif/IVMRWindowlessControl::SetBorderColor
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
 - IVMRWindowlessControl.SetBorderColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



The border color is color used to fill any area of the destination rectangle that does not contain video. It is typically used in two instances: (1) when the video straddles two monitors and (2) when the VMR is trying to maintain the aspect ratio of the movie by letter boxing the video to fit within the specified destination rectangle. See the <a href="https://msdn.microsoft.com/421910fb-8007-4347-a57c-6a46b7b733b3">IVMRWindowlessControl::SetAspectRatioMode</a> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c21c5611-f376-4899-9914-c14a18af3810">IVMRWindowlessControl Interface</a>



<a href="https://msdn.microsoft.com/f0bf04c8-17e6-4e1f-b35f-2e10c9de8b92">IVMRWindowlessControl::GetBorderColor</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

