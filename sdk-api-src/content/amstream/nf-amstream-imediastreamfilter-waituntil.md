---
UID: NF:amstream.IMediaStreamFilter.WaitUntil
title: IMediaStreamFilter::WaitUntil method
author: windows-driver-content
description: Note  This interface is deprecated. New applications should not use it. The WaitUntil method causes the filter to block until a specified stream time. The filter's pins call this method. They can interrupt the wait by flushing the filter.
old-location: dshow\imediastreamfilter_waituntil.htm
old-project: DirectShow
ms.assetid: 5669a3c6-b060-49e8-b8e6-2e3617b44d62
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMediaStreamFilter, IMediaStreamFilter interface [DirectShow], WaitUntil method, IMediaStreamFilter::WaitUntil, IMediaStreamFilterWaitUntil, WaitUntil method [DirectShow], WaitUntil method [DirectShow], IMediaStreamFilter interface, WaitUntil,IMediaStreamFilter.WaitUntil, amstream/IMediaStreamFilter::WaitUntil, dshow.imediastreamfilter_waituntil
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: amstream.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AMSI_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	amstream.h
api_name:
-	IMediaStreamFilter.WaitUntil
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IMediaStreamFilter::WaitUntil method


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <b>WaitUntil</b> method causes the filter to block until a specified stream time. The filter's pins call this method. They can interrupt the wait by flushing the filter.




## -parameters




### -param WaitStreamTime [in]

Specifies the stream time, in 100-nanosecond units.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The wait was interrupted.

</td>
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
</table>
 




## -remarks



If the graph does not have a reference clock, the method returns E_FAIL.




## -see-also




<a href="https://msdn.microsoft.com/1ac4976b-7088-47ac-9689-58c143746f05">IMediaStreamFilter Interface</a>
 

 

