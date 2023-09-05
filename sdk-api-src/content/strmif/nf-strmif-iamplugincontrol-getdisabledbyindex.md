---
UID: NF:strmif.IAMPluginControl.GetDisabledByIndex
title: IAMPluginControl::GetDisabledByIndex (strmif.h)
description: IAMPluginControl::GetDisabledByIndex (strmif.h) gets a class identifier (CLSID) from the blocked list.
helpviewer_keywords: ["GetDisabledByIndex","GetDisabledByIndex method [DirectShow]","GetDisabledByIndex method [DirectShow]","IAMPluginControl interface","IAMPluginControl interface [DirectShow]","GetDisabledByIndex method","IAMPluginControl.GetDisabledByIndex","IAMPluginControl::GetDisabledByIndex","dshow.iamplugincontrol_getdisabledbyindex","strmif/IAMPluginControl::GetDisabledByIndex"]
old-location: dshow\iamplugincontrol_getdisabledbyindex.htm
tech.root: DirectShow
ms.assetid: 7c55e37b-46f1-4283-bea4-3884ae730906
ms.date: 4/26/2023
ms.keywords: GetDisabledByIndex, GetDisabledByIndex method [DirectShow], GetDisabledByIndex method [DirectShow],IAMPluginControl interface, IAMPluginControl interface [DirectShow],GetDisabledByIndex method, IAMPluginControl.GetDisabledByIndex, IAMPluginControl::GetDisabledByIndex, dshow.iamplugincontrol_getdisabledbyindex, strmif/IAMPluginControl::GetDisabledByIndex
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
 - IAMPluginControl::GetDisabledByIndex
 - strmif/IAMPluginControl::GetDisabledByIndex
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
 - IAMPluginControl.GetDisabledByIndex
---

# IAMPluginControl::GetDisabledByIndex


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Gets a class identifier (CLSID) from the blocked list.

## -parameters

### -param index [in]

The zero-based index of the CLSID to retrieve.

### -param clsid [out]

Receives the CLSID at the specified index.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NO_MORE_ITEMS)</b></dt>
</dl>
</td>
<td width="60%">
The <i>index</i> parameter is out of range.


</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-iamplugincontrol">IAMPluginControl</a>



<a href="/windows/desktop/DirectShow/intelligent-connect">Intelligent Connect</a>