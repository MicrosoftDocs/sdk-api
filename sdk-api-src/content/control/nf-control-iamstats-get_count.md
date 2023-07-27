---
UID: NF:control.IAMStats.get_Count
title: IAMStats::get_Count (control.h)
description: The get_Count method retrieves the number of statistics.
helpviewer_keywords: ["IAMStats interface [DirectShow]","get_Count method","IAMStats.get_Count","IAMStats::get_Count","IAMStatsget_Count","control/IAMStats::get_Count","dshow.iamstats_get_count","get_Count","get_Count method [DirectShow]","get_Count method [DirectShow]","IAMStats interface"]
old-location: dshow\iamstats_get_count.htm
tech.root: dshow
ms.assetid: 48f2543a-7c93-4d4f-a568-b8066e9545fd
ms.date: 4/26/2023
ms.keywords: IAMStats interface [DirectShow],get_Count method, IAMStats.get_Count, IAMStats::get_Count, IAMStatsget_Count, control/IAMStats::get_Count, dshow.iamstats_get_count, get_Count, get_Count method [DirectShow], get_Count method [DirectShow],IAMStats interface
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IAMStats::get_Count
 - control/IAMStats::get_Count
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
 - IAMStats.get_Count
---

# IAMStats::get_Count


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_Count</code> method retrieves the number of statistics.

## -parameters

### -param plCount [out]

Receives the number of statistics.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-iamstats">IAMStats Interface</a>