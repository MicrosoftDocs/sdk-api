---
UID: NF:strmif.IMediaFilter.Run
title: IMediaFilter::Run
author: windows-sdk-content
description: The Run method runs the filter.
old-location: dshow\imediafilter_run.htm
tech.root: DirectShow
ms.assetid: ec422312-bbc2-4b66-b2cd-1a9eebd1eee1
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IMediaFilter interface [DirectShow],Run method, IMediaFilter.Run, IMediaFilter::Run, IMediaFilterRun, Run, Run method [DirectShow], Run method [DirectShow],IMediaFilter interface, dshow.imediafilter_run, strmif/IMediaFilter::Run
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
 - IMediaFilter.Run
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
- IMediaFilter.Run
: 
---

# IMediaFilter::Run


## -description



The <code>Run</code> method runs the filter.




## -parameters




### -param tStart

Reference time corresponding to stream time 0.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

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
Transition is not complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success. Transition is complete.

</td>
</tr>
</table>
 




## -remarks



When a filter is running, it can receive, process, and deliver samples. Source filters generate new samples, and renderer filters render them.

The state transition might be asynchronous. If the method returns before the transition completes, the return value is S_FALSE.

Stream time is calculated as the current reference time minus <i>tStart</i>. To calculate when a media sample should be rendered, the renderer compares the time stamp with the current stream time. Thus, a media sample with a time stamp of zero should be rendered at time <i>tStart</i>. For more information, see <a href="https://msdn.microsoft.com/7d883638-5ddb-48b9-9d0b-104944a151e9">Time and Clocks in DirectShow</a>.

When an application calls the <a href="https://msdn.microsoft.com/b52a5fa7-96f8-4949-9cf0-2d526f23bee1">IMediaControl::Run</a> method, the Filter Graph Manager calls <code>IMediaFilter::Run</code> on each filter. It sets the value of <i>tStart</i> slightly in the future, to account for graph latency.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/5c0060e8-a9e5-4141-a38d-9a1bc55cc91b">IMediaFilter Interface</a>
 

 

