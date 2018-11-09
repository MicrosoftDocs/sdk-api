---
UID: NF:strmif.IMediaFilter.Stop
title: IMediaFilter::Stop
author: windows-sdk-content
description: The Stop method stops the filter.
old-location: dshow\imediafilter_stop.htm
tech.root: DirectShow
ms.assetid: 8c415b5c-1aee-4ea4-b182-fd95da4898aa
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IMediaFilter interface [DirectShow],Stop method, IMediaFilter.Stop, IMediaFilter::Stop, IMediaFilterStop, Stop, Stop method [DirectShow], Stop method [DirectShow],IMediaFilter interface, dshow.imediafilter_stop, strmif/IMediaFilter::Stop
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
 - IMediaFilter.Stop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaFilter::Stop


## -description



The <code>Stop</code> method stops the filter.




## -parameters






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



When a filter is stopped, it does not process or deliver any samples, and it rejects samples from upstream filters.

The state transition might be asynchronous. If the method returns before the transition completes, the return value is S_FALSE.

This method always sets the filter's state to State_Stopped, even if the method returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/41f88abc-57d1-4f80-a099-d17e624ab8a6">FILTER_STATE Enumeration</a>



<a href="https://msdn.microsoft.com/5c0060e8-a9e5-4141-a38d-9a1bc55cc91b">IMediaFilter Interface</a>
 

 

