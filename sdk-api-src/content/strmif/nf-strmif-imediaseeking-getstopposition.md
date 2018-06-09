---
UID: NF:strmif.IMediaSeeking.GetStopPosition
title: IMediaSeeking::GetStopPosition
author: windows-sdk-content
description: The GetStopPosition method retrieves the time at which the playback will stop, relative to the duration of the stream.
old-location: dshow\imediaseeking_getstopposition.htm
old-project: DirectShow
ms.assetid: 7205ea09-65c1-4cd5-b76d-55977b0fbab9
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetStopPosition, GetStopPosition method [DirectShow], GetStopPosition method [DirectShow],IMediaSeeking interface, IMediaSeeking interface [DirectShow],GetStopPosition method, IMediaSeeking.GetStopPosition, IMediaSeeking::GetStopPosition, IMediaSeekingGetStopPosition, dshow.imediaseeking_getstopposition, strmif/IMediaSeeking::GetStopPosition
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
 - IMediaSeeking.GetStopPosition
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMediaSeeking::GetStopPosition


## -description



The <code>GetStopPosition</code> method retrieves the time at which the playback will stop, relative to the duration of the stream.




## -parameters




### -param pStop [out]

Pointer to a variable that receives the stop time, in units of the current time format.


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



The playback rate does not affect the value returned by this method.

The returned value is expressed in the current time format. The default time format is <a href="https://msdn.microsoft.com/862c95bc-2e0a-42c0-b907-45f64f27bd41">REFERENCE_TIME</a> units (100 nanoseconds). To change time formats, use the <a href="https://msdn.microsoft.com/b6f64f8a-67b8-4297-8f0d-389001fa1681">IMediaSeeking::SetTimeFormat</a> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/32adad53-d1ac-495f-9347-7bdd4ae4b78d">IMediaSeeking Interface</a>
 

 

