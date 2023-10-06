---
UID: NF:strmif.IAMExtTransport.GetStatus
title: IAMExtTransport::GetStatus (strmif.h)
description: The GetStatus method returns information about the transport's status.
helpviewer_keywords: ["GetStatus","GetStatus method [DirectShow]","GetStatus method [DirectShow]","IAMExtTransport interface","IAMExtTransport interface [DirectShow]","GetStatus method","IAMExtTransport.GetStatus","IAMExtTransport::GetStatus","IAMExtTransportGetStatus","dshow.iamexttransport_getstatus","strmif/IAMExtTransport::GetStatus"]
old-location: dshow\iamexttransport_getstatus.htm
tech.root: dshow
ms.assetid: 01d90527-4851-45a3-9481-929a9f4aa0cd
ms.date: 4/26/2023
ms.keywords: GetStatus, GetStatus method [DirectShow], GetStatus method [DirectShow],IAMExtTransport interface, IAMExtTransport interface [DirectShow],GetStatus method, IAMExtTransport.GetStatus, IAMExtTransport::GetStatus, IAMExtTransportGetStatus, dshow.iamexttransport_getstatus, strmif/IAMExtTransport::GetStatus
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
 - IAMExtTransport::GetStatus
 - strmif/IAMExtTransport::GetStatus
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
 - IAMExtTransport.GetStatus
---

# IAMExtTransport::GetStatus


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetStatus</code> method returns information about the transport's status.

## -parameters

### -param StatusItem [in]

Specifies the status information to retrieve. See Remarks for more information.

### -param pValue [in, out]

Pointer to variable that either specifies or receives a <b>long</b> integer, whose meaning depends on the value of <i>StatusItem</i>. See Remarks for more information.

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

The <i>StatusItem</i> parameter is a flag that specifies which status information to retrieve. The method returns in the information in the <i>pValue</i> parameter. Not every device supports every status flag. The following flags are defined:

<ul>
<li>ED_MODE: Returns the current transport mode, such as pause or play. See <a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-put_mode">IAMExtTransport::put_Mode</a> for a list of constants that define the transport modes. As an alternative, you can set <i>StatusItem</i> equal to one of these constants, and <i>pValue</i> will receive the value OATRUE if the transport is currently in that mode, or OAFALSE otherwise.</li>
<li>ED_MEDIA_TYPE: Indicates the format of the media for this transport. Returns one of the following constants.<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr>
<td>ED_MEDIA_VHS</td>
<td>VHS</td>
</tr>
<tr>
<td>ED_MEDIA_SVHS</td>
<td>S-VHS</td>
</tr>
<tr>
<td>ED_MEDIA_HI8</td>
<td>Hi-8</td>
</tr>
<tr>
<td>ED_MEDIA_UMATIC</td>
<td>Umatic</td>
</tr>
<tr>
<td>ED_MEDIA_DVC</td>
<td>DV tape (DVC)</td>
</tr>
<tr>
<td>ED_MEDIA_1_INCH</td>
<td>1-inch tape</td>
</tr>
<tr>
<td>ED_MEDIA_D1</td>
<td>D1 format</td>
</tr>
<tr>
<td>ED_MEDIA_D2</td>
<td>D2 format</td>
</tr>
<tr>
<td>ED_MEDIA_D3</td>
<td>D3 format</td>
</tr>
<tr>
<td>ED_MEDIA_D5</td>
<td>D5 format</td>
</tr>
<tr>
<td>ED_MEDIA_DBETA</td>
<td>Digital Betacam</td>
</tr>
<tr>
<td>ED_MEDIA_BETA</td>
<td>Betacam</td>
</tr>
<tr>
<td>ED_MEDIA_8MM</td>
<td>8-millimeter</td>
</tr>
<tr>
<td>ED_MEDIA_DDR</td>
<td>Digital disk recorder</td>
</tr>
<tr>
<td>ED_MEDIA_SX</td>
<td>Betacam SX</td>
</tr>
<tr>
<td>ED_MEDIA_OTHER</td>
<td>Other</td>
</tr>
<tr>
<td>ED_MEDIA_CLV</td>
<td>CLV (Constant Linear Velocity, or "standard play") laserdisc</td>
</tr>
<tr>
<td>ED_MEDIA_CAV</td>
<td>CAV (Constant Angular Velocity, or "extended play") laserdisc</td>
</tr>
</table>
 

</li>
<li>ED_LINK_MODE: Returns OATRUE if the transport's controls are linked to the filter graph's <b>Run</b>, <b>Stop</b>, and <b>Pause</b> methods, and OAFALSE otherwise. See <a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-put_mode">IAMExtTransport::put_Mode</a> for more information.</li>
<li>ED_MEDIA_PRESENT: Returns OATRUE if the transport's media is present, or OAFALSE otherwise.</li>
<li>ED_MEDIA_LENGTH: Returns the length of the media, in units of the current time format (see <a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-settransportbasicparameters">IAMExtTransport::SetTransportBasicParameters</a>).</li>
<li>ED_MEDIA_TRACK_COUNT: Returns the track count.</li>
<li>ED_MEDIA_TRACK_LENGTH: Returns the track length, in units of the current time format.</li>
<li>ED_MEDIA_SIDE: Indicates which side of the media is active.</li>
</ul>
In Windows XP Service Pack 2 and later, the following additional play modes are defined for ED_MODE.

<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr>
<td>ED_MODE_PLAY_SLOW_FWD_X</td>
<td>Play unspecified slow forward. (Slow-forward play at vendor-specific speed.)</td>
</tr>
<tr>
<td>ED_MODE_PLAY_FAST_FWD_X</td>
<td>Play unspecified fast forward. (Fast-forward play at vendor-specific speed.)</td>
</tr>
<tr>
<td>ED_MODE_PLAY_SLOW_REV_X</td>
<td>Play unspecified slow reverse. (Slow-reverse play at vendor-specific speed.)</td>
</tr>
<tr>
<td>ED_MODE_PLAY_FAST_REV_X</td>
<td>Play unspecified fast reverse. (Fast-reverse play at vendor-specific speed.)</td>
</tr>
<tr>
<td>ED_MODE_STOP_START</td>
<td>Transport is stopped at the beginning of the tape (or other transport medium).</td>
</tr>
<tr>
<td>ED_MODE_STOP_END</td>
<td>Transport is stopped at the end of the tape (or other transport medium).</td>
</tr>
<tr>
<td>ED_MODE_STOP_EMERGENCY</td>
<td>Transport has stopped due to unexpected conditions or to avoid possible damage to the transport.</td>
</tr>
</table>
 

To use these constants, include the header file Xprtdefs.h from the Windows SDK.

<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>

<a href="/windows/desktop/DirectShow/msdv-driver">MSDV</a> supports the following status flags: 

<ul>
<li>ED_MODE: See previous remarks. </li>
<li>ED_MEDIA_TYPE: Returns one of the following values.
<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr>
<td>ED_MEDIA_VHS</td>
<td>VHS tape.</td>
</tr>
<tr>
<td>ED_MEDIA_DVC</td>
<td>DV tape.</td>
</tr>
<tr>
<td>ED_MEDIA_UNKNOWN</td>
<td>Unknown type.</td>
</tr>
<tr>
<td>ED_MEDIA_NOT_PRESENT</td>
<td>The transport is empty. </td>
</tr>
</table>
 

</li>
<li>ED_DEV_REMOVED_HEVENT_GET. Returns a handle to an event. The driver signals the event if the device is physically removed from the system.</li>
<li>ED_DEV_REMOVED_HEVENT_RELEASE. Releases the event handle obtained through the ED_DEV_REMOVED_HEVENT_GET flag. Specify the address of the handle in the pValue parameter. </li>
<li>ED_MODE_CHANGE_NOTIFY. Returns the device state in pValue. If the method returns E_PENDING, a state change is pending. You can use the ED_NOTIFY_HEVENT_GET flag to get notification when the state change is complete. </li>
<li>ED_NOTIFY_HEVENT_GET. Returns a handle to an event. The driver signals the event when the device completes a mode change. </li>
<li>ED_NOTIFY_HEVENT_RELEASE. Releases the event handle obtained through the ED_NOTIFY_HEVENT_GET flag. Specify the address of the handle in the pValue parameter. </li>
</ul>
<h3><a id="MPEG_Camcorder_Implementation"></a><a id="mpeg_camcorder_implementation"></a><a id="MPEG_CAMCORDER_IMPLEMENTATION"></a>MPEG Camcorder Implementation</h3>

<a href="/windows/desktop/DirectShow/mstape-driver">MSTape</a> supports an additional media format for the ED_MEDIA_TYPE flag.

<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr>
<td>ED_MEDIA_NEO</td>
<td>Mini digital tape for MPEG-2 transport stream (D-VHS).</td>
</tr>
</table>
 

Some of these flags are defined in the header file Xptrdefs.h.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>