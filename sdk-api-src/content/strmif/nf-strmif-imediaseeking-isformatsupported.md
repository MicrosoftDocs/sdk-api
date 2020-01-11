---
UID: NF:strmif.IMediaSeeking.IsFormatSupported
title: IMediaSeeking::IsFormatSupported (strmif.h)
description: The IsFormatSupported method determines whether a specified time format is supported for seek operations.
old-location: dshow\imediaseeking_isformatsupported.htm
tech.root: DirectShow
ms.assetid: 443a8dbc-c12a-4d50-9005-1fedf701f6fd
ms.date: 12/05/2018
ms.keywords: IMediaSeeking interface [DirectShow],IsFormatSupported method, IMediaSeeking.IsFormatSupported, IMediaSeeking::IsFormatSupported, IMediaSeekingIsFormatSupported, IsFormatSupported, IsFormatSupported method [DirectShow], IsFormatSupported method [DirectShow],IMediaSeeking interface, dshow.imediaseeking_isformatsupported, strmif/IMediaSeeking::IsFormatSupported
f1_keywords:
- strmif/IMediaSeeking.IsFormatSupported
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IMediaSeeking.IsFormatSupported
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaSeeking::IsFormatSupported


## -description



The <code>IsFormatSupported</code> method determines whether a specified time format is supported for seek operations.




## -parameters




### -param pFormat [in]

Pointer to a GUID that specifies the time format. See <a href="https://docs.microsoft.com/windows/desktop/DirectShow/time-format-guids">Time Format GUIDs</a>.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The format is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The format is supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imediaseeking">IMediaSeeking Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-settimeformat">IMediaSeeking::SetTimeFormat</a>
 

 

