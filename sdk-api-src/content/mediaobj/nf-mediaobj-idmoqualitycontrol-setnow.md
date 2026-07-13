---
UID: NF:mediaobj.IDMOQualityControl.SetNow
title: IDMOQualityControl::SetNow (mediaobj.h)
description: The SetNow method specifies the earliest time stamp that the DMO will deliver.
helpviewer_keywords: ["IDMOQualityControl interface [DirectShow]","SetNow method","IDMOQualityControl.SetNow","IDMOQualityControl::SetNow","IDMOQualityControlSetNow","SetNow","SetNow method [DirectShow]","SetNow method [DirectShow]","IDMOQualityControl interface","dshow.idmoqualitycontrol_setnow","mediaobj/IDMOQualityControl::SetNow"]
old-location: dshow\idmoqualitycontrol_setnow.htm
tech.root: dshow
ms.assetid: 36efee4f-0a06-421f-bc37-688a6499bda7
ms.date: 4/26/2023
ms.keywords: IDMOQualityControl interface [DirectShow],SetNow method, IDMOQualityControl.SetNow, IDMOQualityControl::SetNow, IDMOQualityControlSetNow, SetNow, SetNow method [DirectShow], SetNow method [DirectShow],IDMOQualityControl interface, dshow.idmoqualitycontrol_setnow, mediaobj/IDMOQualityControl::SetNow
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
 - IDMOQualityControl::SetNow
 - mediaobj/IDMOQualityControl::SetNow
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
 - IDMOQualityControl.SetNow
---

# IDMOQualityControl::SetNow


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetNow</code> method specifies the earliest time stamp that the DMO will deliver.

## -parameters

### -param rtNow [in]

Reference time specifying the earliest time stamp to deliver.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure

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

If quality control is enabled, the DMO discards any samples whose time stamp is less than <i>rtNow</i>. Samples whose time stamp is <i>rtNow</i> or later are processed as efficiently as possible. Depending on the implementation, the DMO might drop some samples to keep pace.

If quality control is disabled, this method has no immediate effect. However, the DMO stores the specified reference time. It uses this value if quality control is enabled at a later time. To enable quality control, call the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-idmoqualitycontrol-setstatus">IDMOQualityControl::SetStatus</a> method.

If incoming samples are not time-stamped, the DMO never performs quality control. The application sets the time stamp in the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput">IMediaObject::ProcessInput</a> method.

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol">IDMOQualityControl Interface</a>