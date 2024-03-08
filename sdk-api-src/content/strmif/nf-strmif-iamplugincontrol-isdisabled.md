---
UID: NF:strmif.IAMPluginControl.IsDisabled
title: IAMPluginControl::IsDisabled (strmif.h)
description: Queries whether a class identifier (CLSID) appears in the blocked list. (IAMPluginControl.IsDisabled)
helpviewer_keywords: ["IAMPluginControl interface [DirectShow]","IsDisabled method","IAMPluginControl.IsDisabled","IAMPluginControl::IsDisabled","IsDisabled","IsDisabled method [DirectShow]","IsDisabled method [DirectShow]","IAMPluginControl interface","dshow.iamplugincontrol_isdisabled","strmif/IAMPluginControl::IsDisabled"]
old-location: dshow\iamplugincontrol_isdisabled.htm
tech.root: dshow
ms.assetid: 2d6bae28-7c26-47c4-8633-9ecc60293dc6
ms.date: 4/26/2023
ms.keywords: IAMPluginControl interface [DirectShow],IsDisabled method, IAMPluginControl.IsDisabled, IAMPluginControl::IsDisabled, IsDisabled, IsDisabled method [DirectShow], IsDisabled method [DirectShow],IAMPluginControl interface, dshow.iamplugincontrol_isdisabled, strmif/IAMPluginControl::IsDisabled
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMPluginControl::IsDisabled
 - strmif/IAMPluginControl::IsDisabled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMPluginControl.IsDisabled
---

# IAMPluginControl::IsDisabled


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Queries whether a class identifier (CLSID) appears in the blocked list.

## -parameters

### -param clsid [in]

The CLSID to search for.

## -returns

This method can return one of these values.

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
The specified CLSID appears in the blocked list.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The specified CLSID is not in the blocked list.


</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-iamplugincontrol">IAMPluginControl</a>



<a href="/windows/desktop/DirectShow/intelligent-connect">Intelligent Connect</a>
