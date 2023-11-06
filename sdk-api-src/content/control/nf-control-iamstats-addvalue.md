---
UID: NF:control.IAMStats.AddValue
title: IAMStats::AddValue (control.h)
description: The AddValue method records a new value.
helpviewer_keywords: ["AddValue","AddValue method [DirectShow]","AddValue method [DirectShow]","IAMStats interface","IAMStats interface [DirectShow]","AddValue method","IAMStats.AddValue","IAMStats::AddValue","IAMStatsAddValue","control/IAMStats::AddValue","dshow.iamstats_addvalue"]
old-location: dshow\iamstats_addvalue.htm
tech.root: dshow
ms.assetid: a408b106-702c-4ecc-a424-b4b3588ea58f
ms.date: 4/26/2023
ms.keywords: AddValue, AddValue method [DirectShow], AddValue method [DirectShow],IAMStats interface, IAMStats interface [DirectShow],AddValue method, IAMStats.AddValue, IAMStats::AddValue, IAMStatsAddValue, control/IAMStats::AddValue, dshow.iamstats_addvalue
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
 - IAMStats::AddValue
 - control/IAMStats::AddValue
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
 - IAMStats.AddValue
---

# IAMStats::AddValue


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>AddValue</code> method records a new value.

## -parameters

### -param lIndex [in]

Specifies the index of the statistic.

### -param dValue [in]

Specifies the value to record.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-iamstats">IAMStats Interface</a>