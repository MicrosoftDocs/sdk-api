---
UID: NF:strmif.IAMPluginControl.IsLegacyDisabled
title: IAMPluginControl::IsLegacyDisabled (strmif.h)
description: Queries whether an Audio Compression Manager (ACM) or Video Compression Manager (VCM) codec appears in the blocked list.
helpviewer_keywords: ["IAMPluginControl interface [DirectShow]","IsLegacyDisabled method","IAMPluginControl.IsLegacyDisabled","IAMPluginControl::IsLegacyDisabled","IsLegacyDisabled","IsLegacyDisabled method [DirectShow]","IsLegacyDisabled method [DirectShow]","IAMPluginControl interface","dshow.iamplugincontrol_islegacydisabled","strmif/IAMPluginControl::IsLegacyDisabled"]
old-location: dshow\iamplugincontrol_islegacydisabled.htm
tech.root: dshow
ms.assetid: f67c7a78-1e4f-469a-9cbb-80c37bba80b7
ms.date: 4/26/2023
ms.keywords: IAMPluginControl interface [DirectShow],IsLegacyDisabled method, IAMPluginControl.IsLegacyDisabled, IAMPluginControl::IsLegacyDisabled, IsLegacyDisabled, IsLegacyDisabled method [DirectShow], IsLegacyDisabled method [DirectShow],IAMPluginControl interface, dshow.iamplugincontrol_islegacydisabled, strmif/IAMPluginControl::IsLegacyDisabled
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
 - IAMPluginControl::IsLegacyDisabled
 - strmif/IAMPluginControl::IsLegacyDisabled
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
 - IAMPluginControl.IsLegacyDisabled
---

# IAMPluginControl::IsLegacyDisabled


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Queries whether an Audio Compression Manager (ACM) or Video Compression Manager (VCM) codec appears in the blocked list.

## -parameters

### -param dllName [in]

The name of the DLL that implements the codec.

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
The specified DLL appears in the blocked list.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The specified DLL is not in the blocked list.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-iamplugincontrol">IAMPluginControl</a>



<a href="/windows/desktop/DirectShow/intelligent-connect">Intelligent Connect</a>