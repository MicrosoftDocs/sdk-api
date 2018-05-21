---
UID: NF:vmr9.IVMRMixerControl9.SetProcAmpControl
title: IVMRMixerControl9::SetProcAmpControl
author: windows-driver-content
description: The SetProcAmpControl method sets the image adjustment for the VMR-9.
old-location: dshow\ivmrmixercontrol9_setprocampcontrol.htm
old-project: DirectShow
ms.assetid: 6e2949f5-87e5-4748-bb23-be14452c8c82
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IVMRMixerControl9 interface [DirectShow],SetProcAmpControl method, IVMRMixerControl9.SetProcAmpControl, IVMRMixerControl9::SetProcAmpControl, IVMRMixerControl9SetProcAmpControl, SetProcAmpControl, SetProcAmpControl method [DirectShow], SetProcAmpControl method [DirectShow],IVMRMixerControl9 interface, dshow.ivmrmixercontrol9_setprocampcontrol, vmr9/IVMRMixerControl9::SetProcAmpControl
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
req.typenames: VMR9DeinterlaceTech
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVMRMixerControl9.SetProcAmpControl
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRMixerControl9::SetProcAmpControl


## -description



The <code>SetProcAmpControl</code> method sets the image adjustment for the VMR-9. Image adjustment includes brightness, contrast, hue, and saturation, and is performed by the graphics device. If the graphics driver does not support hardware image adjustment, this method fails.




## -parameters




### -param dwStreamID [in]

Specifies the input stream. This value corresponds to the input pin. For example, the first input pin is stream 0.


### -param lpClrControl [in]

Pointer to a <a href="https://msdn.microsoft.com/c4395344-e659-4e5a-aba0-ee27e65fe2cc">VMR9ProcAmpControl</a> structure that contains the image adjustment settings.


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
Invalid argument. Possible causes of this error include:

<ul>
<li>The stream number is invalid</li>
<li>The value of <b>dwSize</b> in the <b>VMR9ProcAmpControl</b> structure is invalid.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The pin is not connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_VMR_NO_PROCAMP_HW</b></dt>
</dl>
</td>
<td width="60%">
The graphics hardware does not support ProcAmp controls.

</td>
</tr>
</table>
 




## -remarks



Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/f311303a-8270-40b6-8153-e0bd8b232c69">IVMRMixerControl9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

