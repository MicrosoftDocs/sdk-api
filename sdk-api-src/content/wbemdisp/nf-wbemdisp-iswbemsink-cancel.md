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

# ISWbemSink::Cancel


## -description


The 
<b>Cancel</b> method of the 
<a href="https://msdn.microsoft.com/a90777ef-fa26-4bfb-b196-c083a0c92a29">SWbemSink</a> object cancels all outstanding asynchronous operations that are associated with this object sink.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters






## -returns



This method does not return a value.




## -remarks



You cannot cancel only one asynchronous call. If  multiple asynchronous calls are pending that use this object sink, then this method cancels all the asynchronous calls using this object sink. Asynchronous calls that are associated with other object sinks continue unaffected.

You cannot assign this sink to <b>Nothing</b> to cancel an asynchronous operation. You must call the 
<b>Cancel</b> method to make WMI discontinue the operation and free the associated resources. This is very important with lengthy asynchronous operations, such as queries, or operations that never complete, such as 
<a href="https://msdn.microsoft.com/0b0e8313-4ffd-4d4a-8965-d2c6743e7573">ExecNotificationQueryAsync</a>.

<div class="alert"><b>Note</b>  An asynchronous callback allows a non-authenticated user to provide data to the sink. This poses security risks to your scripts and applications. To eliminate the risks, use semisynchronous or synchronous communication.
For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.</div>
<div> </div>
The following example shows you how to cancel an asynchronous call.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>objwbemsink.Cancel()
set objwbemsink= Nothing</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/a90777ef-fa26-4bfb-b196-c083a0c92a29">SWbemSink</a>
 

 

