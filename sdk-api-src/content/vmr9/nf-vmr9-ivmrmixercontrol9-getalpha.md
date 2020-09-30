---
UID: NF:vmr9.IVMRMixerControl9.GetAlpha
title: IVMRMixerControl9::GetAlpha (vmr9.h)
description: The GetAlpha method retrieves the constant alpha value that is applied to this video stream.
helpviewer_keywords: ["GetAlpha","GetAlpha method [DirectShow]","GetAlpha method [DirectShow]","IVMRMixerControl9 interface","IVMRMixerControl9 interface [DirectShow]","GetAlpha method","IVMRMixerControl9.GetAlpha","IVMRMixerControl9::GetAlpha","IVMRMixerControl9GetAlpha","dshow.ivmrmixercontrol9_getalpha","vmr9/IVMRMixerControl9::GetAlpha"]
old-location: dshow\ivmrmixercontrol9_getalpha.htm
tech.root: dshow
ms.assetid: 0806f27c-4728-4492-a2ac-26067b7c0aaa
ms.date: 12/05/2018
ms.keywords: GetAlpha, GetAlpha method [DirectShow], GetAlpha method [DirectShow],IVMRMixerControl9 interface, IVMRMixerControl9 interface [DirectShow],GetAlpha method, IVMRMixerControl9.GetAlpha, IVMRMixerControl9::GetAlpha, IVMRMixerControl9GetAlpha, dshow.ivmrmixercontrol9_getalpha, vmr9/IVMRMixerControl9::GetAlpha
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
 - IVMRMixerControl9::GetAlpha
 - vmr9/IVMRMixerControl9::GetAlpha
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
 - IVMRMixerControl9.GetAlpha
---

# IVMRMixerControl9::GetAlpha


## -description

The <code>GetAlpha</code> method retrieves the constant alpha value that is applied to this video stream.

## -parameters

### -param dwStreamID [in]

Specifies the input stream. This value corresponds to the input pin. For example, the first input pin is stream 0.

### -param pAlpha [out]

Pointer to a variable that receives the current alpha value.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pAlpha</i> is invalid.

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
</table>

## -remarks

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/windows/desktop/api/vmr9/nn-vmr9-ivmrmixercontrol9">IVMRMixerControl9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>