---
UID: NF:strmif.IMediaSeeking.ConvertTimeFormat
title: IMediaSeeking::ConvertTimeFormat
author: windows-sdk-content
description: The ConvertTimeFormat method converts from one time format to another.
old-location: dshow\imediaseeking_converttimeformat.htm
tech.root: DirectShow
ms.assetid: 868ec03e-d4e5-4a1e-914a-6be8933f1c7c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ConvertTimeFormat, ConvertTimeFormat method [DirectShow], ConvertTimeFormat method [DirectShow],IMediaSeeking interface, IMediaSeeking interface [DirectShow],ConvertTimeFormat method, IMediaSeeking.ConvertTimeFormat, IMediaSeeking::ConvertTimeFormat, IMediaSeekingConvertTimeFormat, dshow.imediaseeking_converttimeformat, strmif/IMediaSeeking::ConvertTimeFormat
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
 - IMediaSeeking.ConvertTimeFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaSeeking::ConvertTimeFormat


## -description



The <code>ConvertTimeFormat</code> method converts from one time format to another.




## -parameters




### -param pTarget [out]

Pointer to a variable that receives the converted time.


### -param pTargetFormat [in]

Pointer to a GUID that specifies the target format. If <b>NULL</b>, the current format is used. See <a href="https://msdn.microsoft.com/510c7146-ff3c-4812-a7ad-b4051aa82ef3">Time Format GUIDs</a>.


### -param Source [in]

Time value to be converted.


### -param pSourceFormat [in]

Pointer to a GUID that specifies the format to convert. If <b>NULL</b>, the current format is used. See <a href="https://msdn.microsoft.com/510c7146-ff3c-4812-a7ad-b4051aa82ef3">Time Format GUIDs</a>.


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
Conversion between these types is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method is not supported.

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
 

 

