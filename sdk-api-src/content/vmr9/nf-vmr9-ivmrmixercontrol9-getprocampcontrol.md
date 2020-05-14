---
UID: NF:vmr9.IVMRMixerControl9.GetProcAmpControl
title: IVMRMixerControl9::GetProcAmpControl (vmr9.h)
description: The GetProcAmpControl method retrieves the current image adjustment settings for the VMR-9.helpviewer_keywords: ["GetProcAmpControl","GetProcAmpControl method [DirectShow]","GetProcAmpControl method [DirectShow]","IVMRMixerControl9 interface","IVMRMixerControl9 interface [DirectShow]","GetProcAmpControl method","IVMRMixerControl9.GetProcAmpControl","IVMRMixerControl9::GetProcAmpControl","IVMRMixerControl9GetProcAmpControl","dshow.ivmrmixercontrol9_getprocampcontrol","vmr9/IVMRMixerControl9::GetProcAmpControl"]
old-location: dshow\ivmrmixercontrol9_getprocampcontrol.htm
tech.root: DirectShow
ms.assetid: 7f100a5b-48d1-40cc-b4ab-02245afde550
ms.date: 12/05/2018
ms.keywords: GetProcAmpControl, GetProcAmpControl method [DirectShow], GetProcAmpControl method [DirectShow],IVMRMixerControl9 interface, IVMRMixerControl9 interface [DirectShow],GetProcAmpControl method, IVMRMixerControl9.GetProcAmpControl, IVMRMixerControl9::GetProcAmpControl, IVMRMixerControl9GetProcAmpControl, dshow.ivmrmixercontrol9_getprocampcontrol, vmr9/IVMRMixerControl9::GetProcAmpControl
f1_keywords:
- vmr9/IVMRMixerControl9.GetProcAmpControl
dev_langs:
- c++
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
- IVMRMixerControl9.GetProcAmpControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRMixerControl9::GetProcAmpControl


## -description



The <code>GetProcAmpControl</code> method retrieves the current image adjustment settings for the VMR-9. Image adjustment includes brightness, contrast, hue, and saturation, and is performed by the graphics device. If the graphics driver does not support hardware image adjustment, this method fails.




## -parameters




### -param dwStreamID [in]

Specifies the input stream. This value corresponds to the input pin. For example, the first input pin is stream 0.


### -param lpClrControl [in, out]

Pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9procampcontrol">VMR9ProcAmpControl</a> structure that receives the image adjustment settings. When the method returns, the <b>dwFlags</b> field indicates which properties are supported by the graphics driver. Set the <b>dwSize</b> member in the structure before calling this method.


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




<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nn-vmr9-ivmrmixercontrol9">IVMRMixerControl9 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

