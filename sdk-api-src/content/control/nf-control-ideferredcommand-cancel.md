---
UID: NF:control.IDeferredCommand.Cancel
title: IDeferredCommand::Cancel (control.h)
description: The Cancel method cancels a command that the application previously queued.
helpviewer_keywords: ["Cancel","Cancel method [DirectShow]","Cancel method [DirectShow]","IDeferredCommand interface","IDeferredCommand interface [DirectShow]","Cancel method","IDeferredCommand.Cancel","IDeferredCommand::Cancel","IDeferredCommandCancel","control/IDeferredCommand::Cancel","dshow.ideferredcommand_cancel"]
old-location: dshow\ideferredcommand_cancel.htm
tech.root: dshow
ms.assetid: 56618860-3655-42a2-ad74-ef43da08d001
ms.date: 4/26/2023
ms.keywords: Cancel, Cancel method [DirectShow], Cancel method [DirectShow],IDeferredCommand interface, IDeferredCommand interface [DirectShow],Cancel method, IDeferredCommand.Cancel, IDeferredCommand::Cancel, IDeferredCommandCancel, control/IDeferredCommand::Cancel, dshow.ideferredcommand_cancel
req.header: control.h
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
 - IDeferredCommand::Cancel
 - control/IDeferredCommand::Cancel
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
 - IDeferredCommand.Cancel
---

# IDeferredCommand::Cancel


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Cancel</code> method cancels a command that the application previously queued.



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
<dt><b>VFW_E_ALREADY_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The request was already canceled.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ideferredcommand">IDeferredCommand Interface</a>
