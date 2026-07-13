---
UID: NF:strmif.IAMExtTransport.SetEditProperty
title: IAMExtTransport::SetEditProperty (strmif.h)
description: The SetEditProperty method defines parameters and values associated with an edit event.
helpviewer_keywords: ["IAMExtTransport interface [DirectShow]","SetEditProperty method","IAMExtTransport.SetEditProperty","IAMExtTransport::SetEditProperty","IAMExtTransportSetEditProperty","SetEditProperty","SetEditProperty method [DirectShow]","SetEditProperty method [DirectShow]","IAMExtTransport interface","dshow.iamexttransport_seteditproperty","strmif/IAMExtTransport::SetEditProperty"]
old-location: dshow\iamexttransport_seteditproperty.htm
tech.root: dshow
ms.assetid: 85ac14c7-7b47-4462-98ba-68a73f4c7497
ms.date: 4/26/2023
ms.keywords: IAMExtTransport interface [DirectShow],SetEditProperty method, IAMExtTransport.SetEditProperty, IAMExtTransport::SetEditProperty, IAMExtTransportSetEditProperty, SetEditProperty, SetEditProperty method [DirectShow], SetEditProperty method [DirectShow],IAMExtTransport interface, dshow.iamexttransport_seteditproperty, strmif/IAMExtTransport::SetEditProperty
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
 - IAMExtTransport::SetEditProperty
 - strmif/IAMExtTransport::SetEditProperty
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
 - IAMExtTransport.SetEditProperty
---

# IAMExtTransport::SetEditProperty


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetEditProperty</code> method defines parameters and values associated with an edit event.



This method is not implemented.

## -parameters

### -param EditID [in]

Specifies the edit property set. Use the identifier returned by the <a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-seteditpropertyset">IAMExtTransport::SetEditPropertySet</a> method.

### -param Param [in]

Specifies the edit event parameter. See Remarks for more information.

### -param Value [in]

Specifies the value of the parameter. See Remarks for more information.

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

An edit event consists of one or more edit event parameters. Use the <b>SetEditPropertySet</b> method to create an edit event, and then use this method to specify the edit event parameters for that edit event.

The <i>Param</i> parameter is a flag that specifies the edit event parameter. The <i>Value</i> parameter specifies the value of that parameter. The meaning of <i>Value</i> depends on the flag used in <i>Param</i>:

<ul>
<li>ED_EDIT_HEVENT: Handle to an event. The device will signal the event when the edit event has completed.</li>
<li>ED_EDIT_IMMEDIATE: If the value is OATRUE, the application can switch the device into edit mode by calling <a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-put_mode">IAMExtTransport::put_Mode</a> with the value ED_MODE_EDIT_CUE.</li>
<li>ED_EDIT_MODE: Specifies the editing mode. Use one of the following constants.<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr>
<td>ED_EDIT_MODE_ASSEMBLE</td>
<td>Assemble edit mode.</td>
</tr>
<tr>
<td>ED_EDIT_MODE_INSERT</td>
<td>Insert edit mode.</td>
</tr>
<tr>
<td>ED_EDIT_MODE_CRASH_RECORD</td>
<td>Crash record mode.</td>
</tr>
</table>
 

</li>
<li>ED_EDIT_TRACK: Specifies which track to edit. Use one or more of the following constants. You can combine constants with a bitwise OR.<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr>
<td>ED_VIDEO</td>
<td>Video track</td>
</tr>
<tr>
<td>ED_AUDIO_1 through ED_AUDIO_24</td>
<td>Audio tracks 1 through 24</td>
</tr>
<tr>
<td>ED_AUDIO_ALL</td>
<td>All audio track</td>
</tr>
</table>
 

</li>
<li>ED_EDIT_SRC_INPOINT: Specifies the inpoint on the source, in units of the current time format.</li>
<li>ED_EDIT_SRC_OUTPOINT: Specifies the outpoint on the source, in units of the current time format.</li>
<li>ED_EDIT_REC_INPOINT: Specifies the inpoint on the record device, in units of the current time format.</li>
<li>ED_EDIT_REC_OUTPOINT: Specifies the outpoint on the record device, in units of the current time format.</li>
<li>ED_EDIT_REHEARSE_MODE: Specifies the preview mode. Use one of the following constants.<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr>
<td>ED_EDIT_BVB</td>
<td>Black-video-black (BVB). Display black, then inserted video, then black.</td>
</tr>
<tr>
<td>ED_EDIT_VBV</td>
<td>Video-black-video (VBV). Display recorded video, then black, then recorded video.</td>
</tr>
<tr>
<td>ED_EDIT_VVV</td>
<td>Video-video-video (VVV). Display recorded video, then inserted video, then recorded video.</td>
</tr>
<tr>
<td>ED_EDIT_PERFORM</td>
<td>Do not preview.</td>
</tr>
</table>
 

</li>
<li>ED_EDIT_ABORT: With the value OATRUE, the method halts the edit if it is currently in progress.</li>
<li>ED_EDIT_TIMEOUT: Specifies how long the device will wait for the edit to complete, before timing out.</li>
<li>ED_EDIT_SEEK: With the value OATRUE, the method seeks to a specified point. First call this method with the ED_EDIT_SEEK_MODE flag, to specify the seek point.</li>
<li>ED_EDIT_SEEK_MODE: Specifies a seek point. Use one of the following constants.<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr>
<td>ED_EDIT_SEEK_EDIT_IN</td>
<td>Seek to the inpoint.</td>
</tr>
<tr>
<td>ED_EDIT_SEEK_EDIT_OUT</td>
<td>Seek to the outpoint.</td>
</tr>
<tr>
<td>ED_EDIT_SEEK_PREROLL</td>
<td>Seek to the inpoint preroll.</td>
</tr>
<tr>
<td>ED_EDIT_SEEK_PREROLL_CT</td>
<td>Seek to the inpoint using timecode, then seek back to the preroll point using the control track.</td>
</tr>
<tr>
<td>ED_EDIT_SEEK_BOOKMARK</td>
<td>Seek to the next bookmark.</td>
</tr>
</table>
 

</li>
</ul>
<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>

<a href="/windows/desktop/DirectShow/msdv-driver">MSDV</a> does not support this method. It returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-geteditproperty">IAMExtTransport::GetEditProperty</a>