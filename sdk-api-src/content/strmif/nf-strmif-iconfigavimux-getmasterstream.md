---
UID: NF:strmif.IConfigAviMux.GetMasterStream
title: IConfigAviMux::GetMasterStream (strmif.h)
description: The GetMasterStream method queries which stream will be used to synchronize the other streams in the file.
helpviewer_keywords: ["GetMasterStream","GetMasterStream method [DirectShow]","GetMasterStream method [DirectShow]","IConfigAviMux interface","IConfigAviMux interface [DirectShow]","GetMasterStream method","IConfigAviMux.GetMasterStream","IConfigAviMux::GetMasterStream","IConfigAviMuxGetMasterStream","dshow.iconfigavimux_getmasterstream","strmif/IConfigAviMux::GetMasterStream"]
old-location: dshow\iconfigavimux_getmasterstream.htm
tech.root: dshow
ms.assetid: 2085a510-16d5-4a82-b372-824026203ef6
ms.date: 4/26/2023
ms.keywords: GetMasterStream, GetMasterStream method [DirectShow], GetMasterStream method [DirectShow],IConfigAviMux interface, IConfigAviMux interface [DirectShow],GetMasterStream method, IConfigAviMux.GetMasterStream, IConfigAviMux::GetMasterStream, IConfigAviMuxGetMasterStream, dshow.iconfigavimux_getmasterstream, strmif/IConfigAviMux::GetMasterStream
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
 - IConfigAviMux::GetMasterStream
 - strmif/IConfigAviMux::GetMasterStream
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
 - IConfigAviMux.GetMasterStream
---

# IConfigAviMux::GetMasterStream


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetMasterStream</code> method queries which stream will be used to synchronize the other streams in the file.

## -parameters

### -param pStream [out]

Receives the index of the master stream, or -1 if no master stream was set.

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
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iconfigavimux">IConfigAviMux Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iconfigavimux-setmasterstream">IConfigAviMux::SetMasterStream</a>