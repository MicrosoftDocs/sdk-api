---
UID: NF:msvidctl.IMSVidCtl.get_AudioRendererActive
title: IMSVidCtl::get_AudioRendererActive (msvidctl.h)
description: The get_AudioRendererActive method retrieves the audio renderer that is currently active.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","get_AudioRendererActive method","IMSVidCtl.get_AudioRendererActive","IMSVidCtl::get_AudioRendererActive","IMSVidCtlget_AudioRendererActive","get_AudioRendererActive","get_AudioRendererActive method [Microsoft TV Technologies]","get_AudioRendererActive method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_get_audiorendereractive","msvidctl/IMSVidCtl::get_AudioRendererActive"]
old-location: mstv\imsvidctl_get_audiorendereractive.htm
tech.root: mstv
ms.assetid: 4ac78904-18ca-4bcb-9c0e-15595a756ecd
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_AudioRendererActive method, IMSVidCtl.get_AudioRendererActive, IMSVidCtl::get_AudioRendererActive, IMSVidCtlget_AudioRendererActive, get_AudioRendererActive, get_AudioRendererActive method [Microsoft TV Technologies], get_AudioRendererActive method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_audiorendereractive, msvidctl/IMSVidCtl::get_AudioRendererActive
req.header: msvidctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidCtl::get_AudioRendererActive
 - msvidctl/IMSVidCtl::get_AudioRendererActive
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msvidctl.h
api_name:
 - IMSVidCtl.get_AudioRendererActive
---

# IMSVidCtl::get_AudioRendererActive


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_AudioRendererActive</b> method retrieves the audio renderer that is currently active.

## -parameters

### -param pVal [out]

Receives an <a href="/previous-versions/windows/desktop/mstv/msvidaudiorenderer">IMSVidAudioRenderer</a> interface pointer. The caller must release the interface. If no audio renderer is active, this parameter receives the value <b>NULL</b>.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

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
</table>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_audiorendereractive">IMSVidCtl::put_AudioRendererActive</a>