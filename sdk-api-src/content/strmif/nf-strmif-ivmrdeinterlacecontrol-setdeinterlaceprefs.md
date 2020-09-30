---
UID: NF:strmif.IVMRDeinterlaceControl.SetDeinterlacePrefs
title: IVMRDeinterlaceControl::SetDeinterlacePrefs (strmif.h)
description: The SetDeinterlacePrefs method specifies how the VMR will select a deinterlacing mode if it cannot use the preferred deinterlacing mode.
helpviewer_keywords: ["IVMRDeinterlaceControl interface [DirectShow]","SetDeinterlacePrefs method","IVMRDeinterlaceControl.SetDeinterlacePrefs","IVMRDeinterlaceControl::SetDeinterlacePrefs","IVMRDeinterlaceControlSetDeinterlacePrefs","SetDeinterlacePrefs","SetDeinterlacePrefs method [DirectShow]","SetDeinterlacePrefs method [DirectShow]","IVMRDeinterlaceControl interface","dshow.ivmrdeinterlacecontrol_setdeinterlaceprefs","strmif/IVMRDeinterlaceControl::SetDeinterlacePrefs"]
old-location: dshow\ivmrdeinterlacecontrol_setdeinterlaceprefs.htm
tech.root: dshow
ms.assetid: 5a78b8cc-ecf8-4e0a-87f0-56b7aac6abdd
ms.date: 12/05/2018
ms.keywords: IVMRDeinterlaceControl interface [DirectShow],SetDeinterlacePrefs method, IVMRDeinterlaceControl.SetDeinterlacePrefs, IVMRDeinterlaceControl::SetDeinterlacePrefs, IVMRDeinterlaceControlSetDeinterlacePrefs, SetDeinterlacePrefs, SetDeinterlacePrefs method [DirectShow], SetDeinterlacePrefs method [DirectShow],IVMRDeinterlaceControl interface, dshow.ivmrdeinterlacecontrol_setdeinterlaceprefs, strmif/IVMRDeinterlaceControl::SetDeinterlacePrefs
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVMRDeinterlaceControl::SetDeinterlacePrefs
 - strmif/IVMRDeinterlaceControl::SetDeinterlacePrefs
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
 - IVMRDeinterlaceControl.SetDeinterlacePrefs
---

# IVMRDeinterlaceControl::SetDeinterlacePrefs


## -description

The <b>SetDeinterlacePrefs</b> method specifies how the VMR will select a deinterlacing mode if it cannot use the preferred deinterlacing mode.

## -parameters

### -param dwDeinterlacePrefs [in]

A member of the <a href="/windows/desktop/api/strmif/ne-strmif-vmrdeinterlaceprefs">VMRDeinterlacePrefs</a> enumeration type.

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
Invalid argument.

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

## -remarks

By default, the preferred deinterlacing mode is the first mode reported by the driver. The application can set the preferred mode by calling the <a href="/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-setdeinterlacemode">IVMRDeinterlaceControl::SetDeinterlaceMode</a> method. If the VMR cannot use the preferred mode, it will fall back to another mode as specified by the <i>dwDeinterlacePrefs</i> parameter.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrdeinterlacecontrol">IVMRDeinterlaceControl Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-getdeinterlaceprefs">IVMRDeinterlaceControl::GetDeinterlacePrefs</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>