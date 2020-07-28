---
UID: NF:vmr9.IVMRDeinterlaceControl9.GetDeinterlaceModeCaps
title: IVMRDeinterlaceControl9::GetDeinterlaceModeCaps (vmr9.h)
description: The GetDeinterlaceModeCaps method gets the capabilities of a deinterlacing mode supported by the graphics device driver.
helpviewer_keywords: ["GetDeinterlaceModeCaps","GetDeinterlaceModeCaps method [DirectShow]","GetDeinterlaceModeCaps method [DirectShow]","IVMRDeinterlaceControl9 interface","IVMRDeinterlaceControl9 interface [DirectShow]","GetDeinterlaceModeCaps method","IVMRDeinterlaceControl9.GetDeinterlaceModeCaps","IVMRDeinterlaceControl9::GetDeinterlaceModeCaps","IVMRDeinterlaceControl9GetDeinterlaceModeCaps","dshow.ivmrdeinterlacecontrol9_getdeinterlacemodecaps","vmr9/IVMRDeinterlaceControl9::GetDeinterlaceModeCaps"]
old-location: dshow\ivmrdeinterlacecontrol9_getdeinterlacemodecaps.htm
tech.root: dshow
ms.assetid: 62b71df5-7665-4023-90cd-e426b751c1df
ms.date: 12/05/2018
ms.keywords: GetDeinterlaceModeCaps, GetDeinterlaceModeCaps method [DirectShow], GetDeinterlaceModeCaps method [DirectShow],IVMRDeinterlaceControl9 interface, IVMRDeinterlaceControl9 interface [DirectShow],GetDeinterlaceModeCaps method, IVMRDeinterlaceControl9.GetDeinterlaceModeCaps, IVMRDeinterlaceControl9::GetDeinterlaceModeCaps, IVMRDeinterlaceControl9GetDeinterlaceModeCaps, dshow.ivmrdeinterlacecontrol9_getdeinterlacemodecaps, vmr9/IVMRDeinterlaceControl9::GetDeinterlaceModeCaps
f1_keywords:
- vmr9/IVMRDeinterlaceControl9.GetDeinterlaceModeCaps
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
- IVMRDeinterlaceControl9.GetDeinterlaceModeCaps
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRDeinterlaceControl9::GetDeinterlaceModeCaps


## -description



The <b>GetDeinterlaceModeCaps</b> method gets the capabilities of a deinterlacing mode supported by the graphics device driver.




## -parameters




### -param lpDeinterlaceMode [in]

Pointer to a GUID that identifies the deinterlacing mode. Call the <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes">IVMRDeinterlaceControl9::GetNumberOfDeinterlaceModes</a> method to obtain a list of GUIDs supported by the driver.
          


### -param lpVideoDescription [in]

Pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9videodesc">VMR9VideoDesc</a> structure describing the video to deinterlace.
          Set the <b>dwSize</b> member of the structure before calling the method. 


### -param lpDeinterlaceCaps [out]

Pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9deinterlacecaps">VMR9DeinterlaceCaps</a> structure. Set the <b>dwSize</b> member of the structure before calling the method. The method fills the structure with information about the specified deinterlacing mode.
          


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DDRAW_CAPS_NOT_SUITABLE</b></dt>
</dl>
</td>
<td width="60%">
The video card does not support hardware deinterlacing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_VMR_NO_DEINTERLACE_HW</b></dt>
</dl>
</td>
<td width="60%">
The video card does not support hardware deinterlacing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_VMR_NOT_IN_MIXER_MODE</b></dt>
</dl>
</td>
<td width="60%">
The VMR is not in mixer mode.

</td>
</tr>
</table>
 




## -remarks



The method returns <b>E_INVALIDARG</b> if you do not set the <b>dwSize</b> member in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9videodesc">VMR9VideoDesc</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9deinterlacecaps">VMR9DeinterlaceCaps</a> structures.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nn-vmr9-ivmrdeinterlacecontrol9">IVMRDeinterlaceControl9 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/setting-deinterlace-preferences">Setting Deinterlace Preferences</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a>
 

 

