---
UID: NF:control.IAMStats.GetIndex
title: IAMStats::GetIndex (control.h)
description: The GetIndex method retrieves the index for a named statistic, or creates a new statistic.
helpviewer_keywords: ["GetIndex","GetIndex method [DirectShow]","GetIndex method [DirectShow]","IAMStats interface","IAMStats interface [DirectShow]","GetIndex method","IAMStats.GetIndex","IAMStats::GetIndex","IAMStatsGetIndex","control/IAMStats::GetIndex","dshow.iamstats_getindex"]
old-location: dshow\iamstats_getindex.htm
tech.root: DirectShow
ms.assetid: a5ea650c-42dd-405c-8ad9-6e48cf51353d
ms.date: 4/26/2023
ms.keywords: GetIndex, GetIndex method [DirectShow], GetIndex method [DirectShow],IAMStats interface, IAMStats interface [DirectShow],GetIndex method, IAMStats.GetIndex, IAMStats::GetIndex, IAMStatsGetIndex, control/IAMStats::GetIndex, dshow.iamstats_getindex
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
 - IAMStats::GetIndex
 - control/IAMStats::GetIndex
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
 - IAMStats.GetIndex
---

# IAMStats::GetIndex


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetIndex</code> method retrieves the index for a named statistic, or creates a new statistic.

## -parameters

### -param szName [in]

Specifies the name of the statistic.

### -param lCreate [in]

Specifies whether to create the statistic, if it is not defined already. If the value is <b>TRUE</b>, the method creates a new index for the statistic when it cannot find an existing entry with that name. If the value is <b>FALSE</b>, the method fails when the statistic does not already exist.

### -param plIndex [out]

Receives the index.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
No match for this name.

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