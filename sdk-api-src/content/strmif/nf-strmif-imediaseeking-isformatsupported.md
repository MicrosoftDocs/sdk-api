---
UID: NF:strmif.IMediaSeeking.IsFormatSupported
title: IMediaSeeking::IsFormatSupported
author: windows-sdk-content
description: The IsFormatSupported method determines whether a specified time format is supported for seek operations.
old-location: dshow\imediaseeking_isformatsupported.htm
old-project: DirectShow
ms.assetid: 443a8dbc-c12a-4d50-9005-1fedf701f6fd
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMediaSeeking interface [DirectShow],IsFormatSupported method, IMediaSeeking.IsFormatSupported, IMediaSeeking::IsFormatSupported, IMediaSeekingIsFormatSupported, IsFormatSupported, IsFormatSupported method [DirectShow], IsFormatSupported method [DirectShow],IMediaSeeking interface, dshow.imediaseeking_isformatsupported, strmif/IMediaSeeking::IsFormatSupported
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
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
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMediaSeeking::IsFormatSupported


## -description



The <code>IsFormatSupported</code> method determines whether a specified time format is supported for seek operations.




## -parameters




### -param pFormat [in]

Pointer to a GUID that specifies the time format. See <a href="https://msdn.microsoft.com/510c7146-ff3c-4812-a7ad-b4051aa82ef3">Time Format GUIDs</a>.


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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/32adad53-d1ac-495f-9347-7bdd4ae4b78d">IMediaSeeking Interface</a>



<a href="https://msdn.microsoft.com/b6f64f8a-67b8-4297-8f0d-389001fa1681">IMediaSeeking::SetTimeFormat</a>
 

 

