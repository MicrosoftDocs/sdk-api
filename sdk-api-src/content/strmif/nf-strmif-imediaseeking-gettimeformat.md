---
UID: NF:strmif.IMediaSeeking.GetTimeFormat
title: IMediaSeeking::GetTimeFormat (strmif.h)
description: The GetTimeFormat method retrieves the time format that is currently being used for seek operations.
helpviewer_keywords: ["GetTimeFormat","GetTimeFormat method [DirectShow]","GetTimeFormat method [DirectShow]","IMediaSeeking interface","IMediaSeeking interface [DirectShow]","GetTimeFormat method","IMediaSeeking.GetTimeFormat","IMediaSeeking::GetTimeFormat","IMediaSeekingGetTimeFormat","dshow.imediaseeking_gettimeformat","strmif/IMediaSeeking::GetTimeFormat"]
old-location: dshow\imediaseeking_gettimeformat.htm
tech.root: dshow
ms.assetid: aa6dc75e-f124-4404-b8fd-ef227d8cada0
ms.date: 12/05/2018
ms.keywords: GetTimeFormat, GetTimeFormat method [DirectShow], GetTimeFormat method [DirectShow],IMediaSeeking interface, IMediaSeeking interface [DirectShow],GetTimeFormat method, IMediaSeeking.GetTimeFormat, IMediaSeeking::GetTimeFormat, IMediaSeekingGetTimeFormat, dshow.imediaseeking_gettimeformat, strmif/IMediaSeeking::GetTimeFormat
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
 - IMediaSeeking::GetTimeFormat
 - strmif/IMediaSeeking::GetTimeFormat
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
 - IMediaSeeking.GetTimeFormat
---

# IMediaSeeking::GetTimeFormat


## -description

The <code>GetTimeFormat</code> method retrieves the time format that is currently being used for seek operations.

## -parameters

### -param pFormat [out]

Pointer to a variable that receives a GUID specifying the time format. See <a href="/windows/desktop/DirectShow/time-format-guids">Time Format GUIDs</a>.

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



<a href="/windows/desktop/api/strmif/nn-strmif-imediaseeking">IMediaSeeking Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-settimeformat">IMediaSeeking::SetTimeFormat</a>