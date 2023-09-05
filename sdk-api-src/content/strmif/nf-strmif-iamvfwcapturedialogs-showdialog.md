---
UID: NF:strmif.IAMVfwCaptureDialogs.ShowDialog
title: IAMVfwCaptureDialogs::ShowDialog (strmif.h)
description: The ShowDialog method displays the specified VFW dialog box.
helpviewer_keywords: ["IAMVfwCaptureDialogs interface [DirectShow]","ShowDialog method","IAMVfwCaptureDialogs.ShowDialog","IAMVfwCaptureDialogs::ShowDialog","IAMVfwCaptureDialogsShowDialog","ShowDialog","ShowDialog method [DirectShow]","ShowDialog method [DirectShow]","IAMVfwCaptureDialogs interface","dshow.iamvfwcapturedialogs_showdialog","strmif/IAMVfwCaptureDialogs::ShowDialog"]
old-location: dshow\iamvfwcapturedialogs_showdialog.htm
tech.root: dshow
ms.assetid: 988b68e5-12fb-47c5-8a49-81ba262da739
ms.date: 4/26/2023
ms.keywords: IAMVfwCaptureDialogs interface [DirectShow],ShowDialog method, IAMVfwCaptureDialogs.ShowDialog, IAMVfwCaptureDialogs::ShowDialog, IAMVfwCaptureDialogsShowDialog, ShowDialog, ShowDialog method [DirectShow], ShowDialog method [DirectShow],IAMVfwCaptureDialogs interface, dshow.iamvfwcapturedialogs_showdialog, strmif/IAMVfwCaptureDialogs::ShowDialog
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
 - IAMVfwCaptureDialogs::ShowDialog
 - strmif/IAMVfwCaptureDialogs::ShowDialog
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
 - IAMVfwCaptureDialogs.ShowDialog
---

# IAMVfwCaptureDialogs::ShowDialog


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>ShowDialog</code> method displays the specified VFW dialog box.

## -parameters

### -param iDialog [in]

Dialog box to display. This is a member of the <a href="/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs">VfwCaptureDialogs</a> enumeration.

### -param hwnd [in]

Handle of the dialog box's parent window.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_CANNOT_CONNECT</b></dt>
</dl>
</td>
<td width="60%">
Could not reconnect with the new format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The filter graph is not stopped.

</td>
</tr>
</table>

## -remarks

Stop the filter graph before calling this method. Otherwise, the method fails and returns VFW_E_NOT_STOPPED.

The Video Format dialog (VfwCaptureDialog_Format) may change the video format. If so, the method tries to reconnect the capture filter. If the downstream filter rejects the new format, the method returns VFW_E_CANNOT_CONNECT.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvfwcapturedialogs">IAMVfwCaptureDialogs Interface</a>