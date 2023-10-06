---
UID: NF:control.IAMStats.GetValueByName
title: IAMStats::GetValueByName (control.h)
description: The GetValueByName method retrieves a statistic, by name.
helpviewer_keywords: ["GetValueByName","GetValueByName method [DirectShow]","GetValueByName method [DirectShow]","IAMStats interface","IAMStats interface [DirectShow]","GetValueByName method","IAMStats.GetValueByName","IAMStats::GetValueByName","IAMStatsGetValueByName","control/IAMStats::GetValueByName","dshow.iamstats_getvaluebyname"]
old-location: dshow\iamstats_getvaluebyname.htm
tech.root: dshow
ms.assetid: c380deb0-bd49-4191-8218-d05aef39cb15
ms.date: 4/26/2023
ms.keywords: GetValueByName, GetValueByName method [DirectShow], GetValueByName method [DirectShow],IAMStats interface, IAMStats interface [DirectShow],GetValueByName method, IAMStats.GetValueByName, IAMStats::GetValueByName, IAMStatsGetValueByName, control/IAMStats::GetValueByName, dshow.iamstats_getvaluebyname
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
 - IAMStats::GetValueByName
 - control/IAMStats::GetValueByName
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
 - IAMStats.GetValueByName
---

# IAMStats::GetValueByName


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetValueByName</code> method retrieves a statistic, by name.

## -parameters

### -param szName [in]

Specifies the name of the statistic.

### -param lIndex [out]

Pointer to a variable that receives the index of this statistic.

### -param lCount [out]

Pointer to a variable that receives the number of values that were recorded.

### -param dLast [out]

Pointer to a variable that receives the most recent value that was recorded.

### -param dAverage [out]

Pointer to a variable that receives the average value.

### -param dStdDev [out]

Pointer to a variable that receives the standard deviation of the values. If the count is less than two, the standard deviation is zero.

### -param dMin [out]

Pointer to a variable that receives the minimum value that was recorded.

### -param dMax [out]

Pointer to a variable that receives the maximum value that was recorded.

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