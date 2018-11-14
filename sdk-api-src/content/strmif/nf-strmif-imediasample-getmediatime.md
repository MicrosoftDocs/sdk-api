---
UID: NF:strmif.IMediaSample.GetMediaTime
title: IMediaSample::GetMediaTime
author: windows-sdk-content
description: The GetMediaTime method retrieves the media times for this sample.
old-location: dshow\imediasample_getmediatime.htm
tech.root: DirectShow
ms.assetid: eb2a8fd4-4a25-482c-8509-f43461c708d6
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetMediaTime, GetMediaTime method [DirectShow], GetMediaTime method [DirectShow],IMediaSample interface, IMediaSample interface [DirectShow],GetMediaTime method, IMediaSample.GetMediaTime, IMediaSample::GetMediaTime, IMediaSampleGetMediaTime, dshow.imediasample_getmediatime, strmif/IMediaSample::GetMediaTime
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
 - IMediaSample.GetMediaTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IMediaSample.GetMediaTime
: 
---

# IMediaSample::GetMediaTime


## -description



The <code>GetMediaTime</code> method retrieves the media times for this sample.




## -parameters




### -param pTimeStart [out]

Pointer to a variable that receives the media start time.


### -param pTimeEnd [out]

Pointer to a variable that receives the media stop time.


## -returns



Returns an HRESULT value. Possible values include those shown in the following table.

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
<dt><b>VFW_E_MEDIA_TIME_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
Media times are not set on this sample.

</td>
</tr>
</table>
 




## -remarks



For more information about media times, see <a href="https://msdn.microsoft.com/7d883638-5ddb-48b9-9d0b-104944a151e9">Time and Clocks in DirectShow</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample Interface</a>
 

 

