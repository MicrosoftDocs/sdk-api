---
UID: NF:strmif.IAMExtTransport.GetCapability
title: IAMExtTransport::GetCapability (strmif.h)
description: The GetCapability method retrieves the general capabilities of the transport.
helpviewer_keywords: ["GetCapability","GetCapability method [DirectShow]","GetCapability method [DirectShow]","IAMExtTransport interface","IAMExtTransport interface [DirectShow]","GetCapability method","IAMExtTransport.GetCapability","IAMExtTransport::GetCapability","IAMExtTransportGetCapability","dshow.iamexttransport_getcapability","strmif/IAMExtTransport::GetCapability"]
old-location: dshow\iamexttransport_getcapability.htm
tech.root: dshow
ms.assetid: f5544fd9-2899-4995-9401-a53f59d6400b
ms.date: 4/26/2023
ms.keywords: GetCapability, GetCapability method [DirectShow], GetCapability method [DirectShow],IAMExtTransport interface, IAMExtTransport interface [DirectShow],GetCapability method, IAMExtTransport.GetCapability, IAMExtTransport::GetCapability, IAMExtTransportGetCapability, dshow.iamexttransport_getcapability, strmif/IAMExtTransport::GetCapability
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IAMExtTransport::GetCapability
 - strmif/IAMExtTransport::GetCapability
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
 - IAMExtTransport.GetCapability
---

# IAMExtTransport::GetCapability


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetCapability</code> method retrieves the general capabilities of the transport.

## -parameters

### -param Capability [in]

Specifies the capability to check. See Remarks for more information.

### -param pValue [out]

Pointer to a variable that receives a <b>long</b> integer. See Remarks for more information.

### -param pdblValue [out]

Pointer to a variable that receives a <b>double</b>. See Remarks for more information.

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

The <i>Capability</i> parameter is a flag that specifies which capability to check. The method returns the result either in the <i>pValue</i> parameter or in the <i>pdblValue</i> parameter, depending on the capability flag.

For the following flags, the method returns the value OATRUE or OAFALSE in the <i>pValue</i> parameter. The value OATRUE indicates that the capability is present, while the value OAFALSE indicates it is absent.

<table>
<tr>
<th>Capability Flag
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>ED_TRANSCAP_CAN_ASSEMBLE</td>
<td>Transport can use assemble record mode (record new tracks that link seamlessly to the control track from the previously recorded segment).</td>
</tr>
<tr>
<td>ED_TRANSCAP_CAN_BUMP_PLAY</td>
<td>Transport can synchronize by varying speed.</td>
</tr>
<tr>
<td>ED_TRANSCAP_CAN_DELAY_AUDIO_IN</td>
<td>Transport can perform delayed-in audio edits.</td>
</tr>
<tr>
<td>ED_TRANSCAP_CAN_DELAY_AUDIO_OUT</td>
<td>Transport can perform delayed-out audio edits.</td>
</tr>
<tr>
<td>ED_TRANSCAP_CAN_DELAY_VIDEO_IN</td>
<td>Transport can perform delayed-in video edits.</td>
</tr>
<tr>
<td>ED_TRANSCAP_CAN_DELAY_VIDEO_OUT</td>
<td>Transport can perform delayed-out video edits.</td>
</tr>
<tr>
<td>ED_TRANSCAP_CAN_DETECT_LENGTH</td>
<td>Transport can detect the length of the media.</td>
</tr>
<tr>
<td>ED_TRANSCAP_CAN_EJECT</td>
<td>Transport can eject the media.</td>
</tr>
<tr>
<td>ED_TRANSCAP_CAN_FREEZE</td>
<td>Transport can freeze/pause.</td>
</tr>
<tr>
<td>ED_TRANSCAP_CAN_INSERT</td>
<td>Transport can use insert record mode (record individual tracks while locked to a prerecorded control track).</td>
</tr>
<tr>
<td>ED_TRANSCAP_CAN_PLAY_BACKWARDS</td>
<td>Transport can play backward.</td>
</tr>
<tr>
<td>ED_TRANSCAP_CAN_SET_EE</td>
<td>Transport can show the device's input on its output.</td>
</tr>
<tr>
<td>ED_TRANSCAP_CAN_SET_PB</td>
<td>Transport can show media playback on its output.</td>
</tr>
<tr>
<td>ED_TRANSCAP_FIELD_STEP</td>
<td>Transport responds to a frame advance command by advancing one field.</td>
</tr>
<tr>
<td>ED_TRANSCAP_HAS_CLOCK</td>
<td>Device has a clock.</td>
</tr>
<tr>
<td>ED_TRANSCAP_HAS_DT</td>
<td>Device has dynamic tracking.</td>
</tr>
<tr>
<td>ED_TRANSCAP_HAS_TIMER</td>
<td>Device has a timer.</td>
</tr>
<tr>
<td>ED_TRANSCAP_HAS_TUNER</td>
<td>Device has a tuner.</td>
</tr>
<tr>
<td>ED_TRANSCAP_IS_MASTER</td>
<td>Device is the master clock for synchronizing.</td>
</tr>
<tr>
<td>ED_TRANSCAP_MULTIPLE_EDITS</td>
<td>Device supports multiple edit events.</td>
</tr>
<tr>
<td>ED_TRANSCAP_NEEDS_CUEING</td>
<td>Device must be cued before it performs an edit.</td>
</tr>
<tr>
<td>ED_TRANSCAP_NEEDS_TBC</td>
<td>Device needs to be calibrated.</td>
</tr>
</table>
 

For the following flags, the method returns a numeric value in the <i>pValue</i> parameter.

<table>
<tr>
<td>Capability Flag
            </td>
<td>Returned Value
            </td>
</tr>
<tr>
<td>ED_TRANSCAP_LTC_TRACK</td>
<td>Returns the track number of the LTC timecode track, or ED_ALL if there is no dedicated timecode track.</td>
</tr>
<tr>
<td>ED_TRANSCAP_NUM_AUDIO_TRACKS</td>
<td>Returns the number of audio tracks.</td>
</tr>
</table>
 

For the following flags, the method returns a value in the <i>pdblValue</i> parameter.

<table>
<tr>
<td>Capability Flag
            </td>
<td>Returned Value
            </td>
</tr>
<tr>
<td>ED_TRANSCAP_FWD_SHUTTLE_MAX</td>
<td>Maximum forward speed in shuttle mode, as a multiple of play speed.</td>
</tr>
<tr>
<td>ED_TRANSCAP_FWD_SHUTTLE_MIN</td>
<td>Minimum forward speed in shuttle mode, as a multiple of play speed.</td>
</tr>
<tr>
<td>ED_TRANSCAP_FWD_VARIABLE_MAX</td>
<td>Maximum forward speed, as a multiple of play speed.</td>
</tr>
<tr>
<td>ED_TRANSCAP_FWD_VARIABLE_MIN</td>
<td>Minimum forward speed, as a multiple of play speed.</td>
</tr>
<tr>
<td>ED_TRANSCAP_REV_SHUTTLE_MAX</td>
<td>Maximum reverse speed in shuttle mode, as a multiple of play speed.</td>
</tr>
<tr>
<td>ED_TRANSCAP_REV_SHUTTLE_MIN</td>
<td>Minimum reverse speed in shuttle mode, as a multiple of play speed.</td>
</tr>
<tr>
<td>ED_TRANSCAP_REV_VARIABLE_MAX</td>
<td>Maximum reverse speed, as a multiple of play speed.</td>
</tr>
<tr>
<td>ED_TRANSCAP_REV_VARIABLE_MIN</td>
<td>Minimum reverse speed, as a multiple of play speed.</td>
</tr>
</table>
 

<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>

<a href="/windows/desktop/DirectShow/msdv-driver">MSDV</a> does not support this method. It returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>