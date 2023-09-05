---
UID: NF:mediaobj.IDMOQualityControl.SetStatus
title: IDMOQualityControl::SetStatus (mediaobj.h)
description: The SetStatus method enables or disables quality control.
helpviewer_keywords: ["IDMOQualityControl interface [DirectShow]","SetStatus method","IDMOQualityControl.SetStatus","IDMOQualityControl::SetStatus","IDMOQualityControlSetStatus","SetStatus","SetStatus method [DirectShow]","SetStatus method [DirectShow]","IDMOQualityControl interface","dshow.idmoqualitycontrol_setstatus","mediaobj/IDMOQualityControl::SetStatus"]
old-location: dshow\idmoqualitycontrol_setstatus.htm
tech.root: dshow
ms.assetid: d22a7a23-6623-4a98-9a0c-5195b29781f9
ms.date: 4/26/2023
ms.keywords: IDMOQualityControl interface [DirectShow],SetStatus method, IDMOQualityControl.SetStatus, IDMOQualityControl::SetStatus, IDMOQualityControlSetStatus, SetStatus, SetStatus method [DirectShow], SetStatus method [DirectShow],IDMOQualityControl interface, dshow.idmoqualitycontrol_setstatus, mediaobj/IDMOQualityControl::SetStatus
req.header: mediaobj.h
req.include-header: Dmo.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDMOQualityControl::SetStatus
 - mediaobj/IDMOQualityControl::SetStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IDMOQualityControl.SetStatus
---

# IDMOQualityControl::SetStatus


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetStatus</code> method enables or disables quality control.

## -parameters

### -param dwFlags [in]

Value that specifies whether to enable or disable quality control. Use DMO_QUALITY_STATUS_ENABLED to enable quality control, or zero to disable quality control.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those in the following table.

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
Invalid argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -remarks

With quality control enabled, the DMO attempts to deliver samples on time. It can skip late samples if necessary. With quality control disabled, the DMO delivers every sample. If you enable quality control, call the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-idmoqualitycontrol-setnow">IDMOQualityControl::SetNow</a> method to specify the earliest time stamp that the DMO should process. Otherwise, the call to <code>SetStatus</code> succeeds but the DMO does not perform quality control.

By default, quality control is disabled.

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol">IDMOQualityControl Interface</a>