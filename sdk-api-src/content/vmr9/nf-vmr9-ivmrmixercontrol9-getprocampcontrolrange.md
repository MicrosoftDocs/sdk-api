---
UID: NF:vmr9.IVMRMixerControl9.GetProcAmpControlRange
title: IVMRMixerControl9::GetProcAmpControlRange (vmr9.h)
description: The GetProcAmpControlRange method retrieves the range of values for an image adjustment setting, such as brightness, contrast, hue, or saturation.
helpviewer_keywords: ["GetProcAmpControlRange","GetProcAmpControlRange method [DirectShow]","GetProcAmpControlRange method [DirectShow]","IVMRMixerControl9 interface","IVMRMixerControl9 interface [DirectShow]","GetProcAmpControlRange method","IVMRMixerControl9.GetProcAmpControlRange","IVMRMixerControl9::GetProcAmpControlRange","IVMRMixerControl9GetProcAmpControlRange","dshow.ivmrmixercontrol9_getprocampcontrolrange","vmr9/IVMRMixerControl9::GetProcAmpControlRange"]
old-location: dshow\ivmrmixercontrol9_getprocampcontrolrange.htm
tech.root: dshow
ms.assetid: e7db2b22-b3d2-4c6f-84fc-5a287761ed7a
ms.date: 12/05/2018
ms.keywords: GetProcAmpControlRange, GetProcAmpControlRange method [DirectShow], GetProcAmpControlRange method [DirectShow],IVMRMixerControl9 interface, IVMRMixerControl9 interface [DirectShow],GetProcAmpControlRange method, IVMRMixerControl9.GetProcAmpControlRange, IVMRMixerControl9::GetProcAmpControlRange, IVMRMixerControl9GetProcAmpControlRange, dshow.ivmrmixercontrol9_getprocampcontrolrange, vmr9/IVMRMixerControl9::GetProcAmpControlRange
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVMRMixerControl9::GetProcAmpControlRange
 - vmr9/IVMRMixerControl9::GetProcAmpControlRange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRMixerControl9.GetProcAmpControlRange
---

# IVMRMixerControl9::GetProcAmpControlRange


## -description

The <code>GetProcAmpControlRange</code> method retrieves the range of values for an image adjustment setting, such as brightness, contrast, hue, or saturation. Image adjustment is performed by the graphics device, so the valid range depends on the graphics driver. If the driver does not support hardware image adjustment, this method fails.

## -parameters

### -param dwStreamID [in]

Specifies the input stream. This value corresponds to the input pin. For example, the first input pin is stream 0.

### -param lpClrControl [in, out]

Pointer to a <a href="/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9procampcontrolrange">VMR9ProcAmpControlRange</a> structure that receives the range. The caller must set the <b>dwSize</b> and <b>dwProperty</b> fields.

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
<li>The value of <b>dwSize</b> or <b>dwProperty</b> in the <b>VMR9ProcAmpControl</b> structure is invalid.</li>
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

<a href="/windows/desktop/api/vmr9/nn-vmr9-ivmrmixercontrol9">IVMRMixerControl9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>