---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IWMReaderAdvanced::DeliverTime


## -description



The <b>DeliverTime</b> method provides the reader with a clock time. Use this method only when the application is providing the clock.




## -parameters




### -param cnsTime [in]

The time, in 100-nanosecond units.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
</table>
 




## -remarks



Before making the first call to this method, call the <a href="https://msdn.microsoft.com/1f29beea-1da4-41e0-a68d-93af3b1f55ed">IWMReaderAdvanced::SetUserProvidedClock</a> method with the value <b>TRUE</b>, to specify that the application is providing the clock. Otherwise, the <b>DeliverTime</b> method returns E_UNEXPECTED.

After <b>DeliverTime</b> is called, the reader reads data as fast as possible until it reaches the specified time. When the reader reaches that time, it calls <a href="https://msdn.microsoft.com/9913bbc4-df59-484f-b050-324e2ecdeb1c">IWMReaderCallbackAdvanced::OnTime</a>, and then sends samples to the callback.

In general, the value of <i>cnsTime</i> should increase each time the method is called (that is, the clock should run forward). However, sometimes it may be possible to pass a smaller value. The <b>DeliverTime</b> method is asynchronous, meaning the reader object reads the data on another thread. The application can specify a smaller time value only if the reader object has not reached that point in the file. For example, if the application calls <b>DeliverTime</b> with the value 100 seconds, and immediately calls it again with the value 50 seconds, the call would probably succeed, because the reader object will not reach the 50-second point in the file. However, you cannot be sure the call will succeed in this case, because the application does not control the reader's thread.




## -see-also




<a href="https://msdn.microsoft.com/1b04f361-8147-4f6a-8c9d-d8eeed28550a">Broadcasting ASF Data</a>



<a href="https://msdn.microsoft.com/a7a20f87-6f21-4fe8-8889-1b6689daf833">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/5d741e49-9fdf-4f8d-9ea1-faaecf879be4">IWMReaderAdvanced2</a>
 

 

