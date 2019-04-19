---
UID: NF:strmif.IMediaSeeking.IsUsingTimeFormat
title: IMediaSeeking::IsUsingTimeFormat (strmif.h)
author: windows-sdk-content
description: The IsUsingTimeFormat method determines whether seek operations are currently using a specified time format.
old-location: dshow\imediaseeking_isusingtimeformat.htm
tech.root: DirectShow
ms.assetid: 27211946-9b05-40fc-823e-efad87a730a3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMediaSeeking interface [DirectShow],IsUsingTimeFormat method, IMediaSeeking.IsUsingTimeFormat, IMediaSeeking::IsUsingTimeFormat, IMediaSeekingIsUsingTimeFormat, IsUsingTimeFormat, IsUsingTimeFormat method [DirectShow], IsUsingTimeFormat method [DirectShow],IMediaSeeking interface, dshow.imediaseeking_isusingtimeformat, strmif/IMediaSeeking::IsUsingTimeFormat
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
 - IMediaSeeking.IsUsingTimeFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaSeeking::IsUsingTimeFormat


## -description



The <code>IsUsingTimeFormat</code> method determines whether seek operations are currently using a specified time format.




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
The specified format is not the current format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The specified format is the current format.

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
 




## -remarks



This method is slightly more efficient than the <a href="https://msdn.microsoft.com/aa6dc75e-f124-4404-b8fd-ef227d8cada0">IMediaSeeking::GetTimeFormat</a> method, because it does not require copying the GUID.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/32adad53-d1ac-495f-9347-7bdd4ae4b78d">IMediaSeeking Interface</a>



<a href="https://msdn.microsoft.com/b6f64f8a-67b8-4297-8f0d-389001fa1681">IMediaSeeking::SetTimeFormat</a>
 

 

