---
UID: NF:strmif.IAMExtTransport.SetChase
title: IAMExtTransport::SetChase (strmif.h)
description: The SetChase method enables or disables chase mode.
helpviewer_keywords: ["IAMExtTransport interface [DirectShow]","SetChase method","IAMExtTransport.SetChase","IAMExtTransport::SetChase","IAMExtTransportSetChase","SetChase","SetChase method [DirectShow]","SetChase method [DirectShow]","IAMExtTransport interface","dshow.iamexttransport_setchase","strmif/IAMExtTransport::SetChase"]
old-location: dshow\iamexttransport_setchase.htm
tech.root: dshow
ms.assetid: f8c94e74-e243-4fa9-85e6-8c027b514e4f
ms.date: 4/26/2023
ms.keywords: IAMExtTransport interface [DirectShow],SetChase method, IAMExtTransport.SetChase, IAMExtTransport::SetChase, IAMExtTransportSetChase, SetChase, SetChase method [DirectShow], SetChase method [DirectShow],IAMExtTransport interface, dshow.iamexttransport_setchase, strmif/IAMExtTransport::SetChase
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
 - IAMExtTransport::SetChase
 - strmif/IAMExtTransport::SetChase
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
 - IAMExtTransport.SetChase
---

# IAMExtTransport::SetChase


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetChase</code> method enables or disables chase mode.



This method is not implemented.

## -parameters

### -param Enable [in]

Specifies whether chase is enabled as a <b>long</b> integer.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>OATRUE</td>
<td>Enable chase.</td>
</tr>
<tr>
<td>OAFALSE</td>
<td>Disable chase.</td>
</tr>
</table>

### -param Offset [in]

Specifies the offset that the transport will maintain from a reference time. The offset is given in the current time format; see <a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-settransportbasicparameters">IAMExtTransport::SetTransportBasicParameters</a> for more information.

### -param hEvent [in]

Specifies a handle to an event. The device signals the event after it has established the signal offset.

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

Use this method when you want an external transport to follow a timecode signal by a fixed offset. For example, if a VCR supports chasing, it can switch to play mode and keep the tape at a fixed offset from a reference timecode.

Chase mode remains in effect until it completes or is canceled. The filter must verify that the transport is maintaining the fixed offset, by periodically reading the transport's timecode.

<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>

<a href="/windows/desktop/DirectShow/msdv-driver">MSDV</a> does not support this method. It returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-getchase">IAMExtTransport::GetChase</a>