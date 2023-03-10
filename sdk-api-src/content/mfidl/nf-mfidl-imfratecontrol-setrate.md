---
UID: NF:mfidl.IMFRateControl.SetRate
title: IMFRateControl::SetRate (mfidl.h)
description: Sets the playback rate. (IMFRateControl.SetRate)
helpviewer_keywords: ["428d73fa-f284-4861-a41e-04ea7709db0f","IMFRateControl interface [Media Foundation]","SetRate method","IMFRateControl.SetRate","IMFRateControl::SetRate","SetRate","SetRate method [Media Foundation]","SetRate method [Media Foundation]","IMFRateControl interface","mf.imfratecontrol_setrate","mfidl/IMFRateControl::SetRate"]
old-location: mf\imfratecontrol_setrate.htm
tech.root: mf
ms.assetid: 428d73fa-f284-4861-a41e-04ea7709db0f
ms.date: 12/05/2018
ms.keywords: 428d73fa-f284-4861-a41e-04ea7709db0f, IMFRateControl interface [Media Foundation],SetRate method, IMFRateControl.SetRate, IMFRateControl::SetRate, SetRate, SetRate method [Media Foundation], SetRate method [Media Foundation],IMFRateControl interface, mf.imfratecontrol_setrate, mfidl/IMFRateControl::SetRate
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFRateControl::SetRate
 - mfidl/IMFRateControl::SetRate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFRateControl.SetRate
---

# IMFRateControl::SetRate


## -description

Sets the playback rate.

## -parameters

### -param fThin [in]

If <b>TRUE</b>, the media streams are thinned. Otherwise, the stream is not thinned. For media sources and demultiplexers, the object must thin the streams when this parameter is <b>TRUE</b>. For downstream transforms, such as decoders and multiplexers, this parameter is informative; it notifies the object that the input streams are thinned. For information, see <a href="/windows/desktop/medfound/about-rate-control">About Rate Control</a>.

### -param flRate [in]

The requested playback rate. Positive values indicate forward playback, negative values indicate reverse playback, and zero indicates scrubbing (the source delivers a single frame).

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<dt><b>MF_E_REVERSE_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The object does not support reverse playback.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_THINNING_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The object does not support thinning.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_RATE</b></dt>
</dl>
</td>
<td width="60%">
The object does not support the requested playback rate.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_RATE_TRANSITION</b></dt>
</dl>
</td>
<td width="60%">
The object cannot change to the new rate while in the running state.
              

</td>
</tr>
</table>

## -remarks

The Media Session prevents some transitions between rate boundaries, depending on the current playback state:

<table>
<tr>
<th>Playback State</th>
<th>Forward/Reverse</th>
<th>Forward/Zero</th>
<th>Reverse/Zero</th>
</tr>
<tr>
<td>Running</td>
<td>No</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<td>Paused</td>
<td>No</td>
<td>Yes</td>
<td>No</td>
</tr>
<tr>
<td>Stopped</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
</tr>
</table>
 

If the transition is not supported, the method returns <b>MF_E_UNSUPPORTED_RATE_TRANSITION</b>.

When a media source completes a call to <b>SetRate</b>, it sends the <a href="/windows/desktop/medfound/mesourceratechanged">MESourceRateChanged</a> event. Other pipeline components do not send this event.

If a media source switches between thinned and non-thinned playback, the streams send an <a href="/windows/desktop/medfound/mestreamthinmode">MEStreamThinMode</a> event to indicate the transition. Events from the media source are not synchronized with events from the media streams. After you receive the <a href="/windows/desktop/medfound/mesourceratechanged">MESourceRateChanged</a> event, you can still receive samples that were queued before the stream switched to thinned or non-thinned mode. The MEStreamThinMode event marks the exact point in the stream where the transition occurs.

When the Media Session completes a call to <b>SetRate</b>, it sends the <a href="/windows/desktop/medfound/mesessionratechanged">MESessionRateChanged</a> event.

## -see-also

<a href="/windows/desktop/medfound/how-to-set-the-playback-rate-on-the-media-session">How to Set the Playback Rate on the Media Session</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol">IMFRateControl</a>
