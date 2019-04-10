---
UID: NF:strmif.IMediaSeeking.GetRate
title: IMediaSeeking::GetRate (strmif.h)
author: windows-sdk-content
description: The GetRate method retrieves the playback rate.
old-location: dshow\imediaseeking_getrate.htm
tech.root: DirectShow
ms.assetid: 419b223d-95b9-4df6-8b65-56846faa6afe
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRate, GetRate method [DirectShow], GetRate method [DirectShow],IMediaSeeking interface, IMediaSeeking interface [DirectShow],GetRate method, IMediaSeeking.GetRate, IMediaSeeking::GetRate, IMediaSeekingGetRate, dshow.imediaseeking_getrate, strmif/IMediaSeeking::GetRate
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
 - IMediaSeeking.GetRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaSeeking::GetRate


## -description



The <code>GetRate</code> method retrieves the playback rate.




## -parameters




### -param pdRate [out]

Pointer to a variable that receives the playback rate.


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
 




## -remarks



The playback rate is expressed as a ratio of the normal speed. Thus, 1.0 is normal playback speed, 0.5 is half speed, and 2.0 is twice speed.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/32adad53-d1ac-495f-9347-7bdd4ae4b78d">IMediaSeeking Interface</a>
 

 

