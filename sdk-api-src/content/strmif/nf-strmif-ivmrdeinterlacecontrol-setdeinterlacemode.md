---
UID: NF:strmif.IVMRDeinterlaceControl.SetDeinterlaceMode
title: IVMRDeinterlaceControl::SetDeinterlaceMode (strmif.h)
description: The SetDeinterlaceMode method sets the deinterlacing mode for the specified video stream.
helpviewer_keywords: ["IVMRDeinterlaceControl interface [DirectShow]","SetDeinterlaceMode method","IVMRDeinterlaceControl.SetDeinterlaceMode","IVMRDeinterlaceControl::SetDeinterlaceMode","IVMRDeinterlaceControlSetDeinterlaceMode","SetDeinterlaceMode","SetDeinterlaceMode method [DirectShow]","SetDeinterlaceMode method [DirectShow]","IVMRDeinterlaceControl interface","dshow.ivmrdeinterlacecontrol_setdeinterlacemode","strmif/IVMRDeinterlaceControl::SetDeinterlaceMode"]
old-location: dshow\ivmrdeinterlacecontrol_setdeinterlacemode.htm
tech.root: dshow
ms.assetid: 1a716e10-5382-4b2b-9a4b-b3998a584956
ms.date: 12/05/2018
ms.keywords: IVMRDeinterlaceControl interface [DirectShow],SetDeinterlaceMode method, IVMRDeinterlaceControl.SetDeinterlaceMode, IVMRDeinterlaceControl::SetDeinterlaceMode, IVMRDeinterlaceControlSetDeinterlaceMode, SetDeinterlaceMode, SetDeinterlaceMode method [DirectShow], SetDeinterlaceMode method [DirectShow],IVMRDeinterlaceControl interface, dshow.ivmrdeinterlacecontrol_setdeinterlacemode, strmif/IVMRDeinterlaceControl::SetDeinterlaceMode
f1_keywords:
- strmif/IVMRDeinterlaceControl.SetDeinterlaceMode
dev_langs:
- c++
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
- IVMRDeinterlaceControl.SetDeinterlaceMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRDeinterlaceControl::SetDeinterlaceMode


## -description


The <b>SetDeinterlaceMode</b> method sets the deinterlacing mode for the specified video stream.


## -parameters




### -param dwStreamID [in]

Index of the video stream to set. To set all streams, use the value 0xFFFFFFFF.


### -param lpDeinterlaceMode [in]

Pointer to a GUID that specifies the deinterlacing mode. To turn off deinterlacing, use the value GUID_NULL.


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
 




## -remarks



If the application does not specify the mode, the VMR defaults to the first mode reported by the driver. In either case, if the VMR cannot use the preferred mode, it falls back to another mode as specified in the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-setdeinterlaceprefs">IVMRDeinterlaceControl::SetDeinterlacePrefs</a> method.

The <b>SetDeinterlaceMode</b> method is effective only for new connections made to the VMR. Some deinterlacing modes require additional reference samples; the exact number depends on the mode. The VMR allocates surfaces for these additional samples. The client must set the deinterlace mode before the surfaces have been allocated. Surface allocation occurs after any of the following:

<ul>
<li>Pin connections, including dynamic reconnections</li>
<li>Dynamic format changes (the upstream filter calls <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-receiveconnection">IPin::ReceiveConnection</a> to specify a new format)</li>
<li>Resolution changes</li>
<li>Monitor changes</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrdeinterlacecontrol">IVMRDeinterlaceControl Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-getdeinterlacemode">IVMRDeinterlaceControl::GetDeinterlaceMode</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

