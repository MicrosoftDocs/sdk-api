---
UID: NF:mediaobj.IDMOQualityControl.GetStatus
title: IDMOQualityControl::GetStatus (mediaobj.h)
description: The GetStatus method determines whether quality control is active.
helpviewer_keywords: ["GetStatus","GetStatus method [DirectShow]","GetStatus method [DirectShow]","IDMOQualityControl interface","IDMOQualityControl interface [DirectShow]","GetStatus method","IDMOQualityControl.GetStatus","IDMOQualityControl::GetStatus","IDMOQualityControlGetStatus","dshow.idmoqualitycontrol_getstatus","mediaobj/IDMOQualityControl::GetStatus"]
old-location: dshow\idmoqualitycontrol_getstatus.htm
tech.root: dshow
ms.assetid: 5c45874f-5546-40cc-a113-bea92bd9784b
ms.date: 4/26/2023
ms.keywords: GetStatus, GetStatus method [DirectShow], GetStatus method [DirectShow],IDMOQualityControl interface, IDMOQualityControl interface [DirectShow],GetStatus method, IDMOQualityControl.GetStatus, IDMOQualityControl::GetStatus, IDMOQualityControlGetStatus, dshow.idmoqualitycontrol_getstatus, mediaobj/IDMOQualityControl::GetStatus
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
 - IDMOQualityControl::GetStatus
 - mediaobj/IDMOQualityControl::GetStatus
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
 - IDMOQualityControl.GetStatus
---

# IDMOQualityControl::GetStatus


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetStatus</code> method determines whether quality control is active.

## -parameters

### -param pdwFlags [out]

Pointer to a variable that receives the quality control status. If quality control is disabled, the value is zero. If quality control is enabled, the value is DMO_QUALITY_STATUS_ENABLED.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer value

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

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol">IDMOQualityControl Interface</a>