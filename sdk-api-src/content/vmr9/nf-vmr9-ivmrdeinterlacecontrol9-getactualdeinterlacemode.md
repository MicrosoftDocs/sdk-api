---
UID: NF:vmr9.IVMRDeinterlaceControl9.GetActualDeinterlaceMode
title: IVMRDeinterlaceControl9::GetActualDeinterlaceMode (vmr9.h)
description: The GetActualDeinterlaceMode method returns the deinterlacing mode that the VMR is using for a specified stream.
helpviewer_keywords: ["GetActualDeinterlaceMode","GetActualDeinterlaceMode method [DirectShow]","GetActualDeinterlaceMode method [DirectShow]","IVMRDeinterlaceControl9 interface","IVMRDeinterlaceControl9 interface [DirectShow]","GetActualDeinterlaceMode method","IVMRDeinterlaceControl9.GetActualDeinterlaceMode","IVMRDeinterlaceControl9::GetActualDeinterlaceMode","IVMRDeinterlaceControl9GetActualDeinterlaceMode","dshow.ivmrdeinterlacecontrol9_getactualdeinterlacemode","vmr9/IVMRDeinterlaceControl9::GetActualDeinterlaceMode"]
old-location: dshow\ivmrdeinterlacecontrol9_getactualdeinterlacemode.htm
tech.root: dshow
ms.assetid: d8b8b92a-c5ed-45fc-8177-1fd5f5a5625b
ms.date: 12/05/2018
ms.keywords: GetActualDeinterlaceMode, GetActualDeinterlaceMode method [DirectShow], GetActualDeinterlaceMode method [DirectShow],IVMRDeinterlaceControl9 interface, IVMRDeinterlaceControl9 interface [DirectShow],GetActualDeinterlaceMode method, IVMRDeinterlaceControl9.GetActualDeinterlaceMode, IVMRDeinterlaceControl9::GetActualDeinterlaceMode, IVMRDeinterlaceControl9GetActualDeinterlaceMode, dshow.ivmrdeinterlacecontrol9_getactualdeinterlacemode, vmr9/IVMRDeinterlaceControl9::GetActualDeinterlaceMode
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
 - IVMRDeinterlaceControl9::GetActualDeinterlaceMode
 - vmr9/IVMRDeinterlaceControl9::GetActualDeinterlaceMode
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
 - IVMRDeinterlaceControl9.GetActualDeinterlaceMode
---

# IVMRDeinterlaceControl9::GetActualDeinterlaceMode


## -description

The <b>GetActualDeinterlaceMode</b> method returns the deinterlacing mode that the VMR is using for a specified stream.

## -parameters

### -param dwStreamID [in]

Index of the video stream.

### -param lpDeinterlaceMode [out]

Pointer to a variable that receives a GUID value that identifies the deinterlacing mode. The method returns GUID_NULL if the VMR has not initialized the deinterlacing hardware, or if the VMR determines that this stream should not be deinterlaced.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream number.

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
<dt><b>VFW_E_VMR_NOT_IN_MIXER_MODE</b></dt>
</dl>
</td>
<td width="60%">
The VMR is not in mixer mode.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vmr9/nn-vmr9-ivmrdeinterlacecontrol9">IVMRDeinterlaceControl9 Interface</a>



<a href="/windows/desktop/DirectShow/setting-deinterlace-preferences">Setting Deinterlace Preferences</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>



<a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a>