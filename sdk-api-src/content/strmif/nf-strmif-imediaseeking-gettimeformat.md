---
UID: NF:strmif.IMediaSeeking.GetTimeFormat
title: IMediaSeeking::GetTimeFormat
author: windows-sdk-content
description: The GetTimeFormat method retrieves the time format that is currently being used for seek operations.
old-location: dshow\imediaseeking_gettimeformat.htm
tech.root: DirectShow
ms.assetid: aa6dc75e-f124-4404-b8fd-ef227d8cada0
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetTimeFormat, GetTimeFormat method [DirectShow], GetTimeFormat method [DirectShow],IMediaSeeking interface, IMediaSeeking interface [DirectShow],GetTimeFormat method, IMediaSeeking.GetTimeFormat, IMediaSeeking::GetTimeFormat, IMediaSeekingGetTimeFormat, dshow.imediaseeking_gettimeformat, strmif/IMediaSeeking::GetTimeFormat
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMediaSeeking.GetTimeFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaSeeking::GetTimeFormat


## -description



The <code>GetTimeFormat</code> method retrieves the time format that is currently being used for seek operations.




## -parameters




### -param pFormat [out]

Pointer to a variable that receives a GUID specifying the time format. See <a href="https://msdn.microsoft.com/510c7146-ff3c-4812-a7ad-b4051aa82ef3">Time Format GUIDs</a>.


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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/32adad53-d1ac-495f-9347-7bdd4ae4b78d">IMediaSeeking Interface</a>



<a href="https://msdn.microsoft.com/b6f64f8a-67b8-4297-8f0d-389001fa1681">IMediaSeeking::SetTimeFormat</a>
 

 

