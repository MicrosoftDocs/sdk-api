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

# IMFASFMultiplexer::GetNextPacket


## -description



Retrieves the next output ASF packet from the multiplexer.




## -parameters




### -param pdwStatusFlags [out]


            Receives zero or more status flags. If more than one packet is waiting, the method sets the <b>ASF_STATUSFLAGS_INCOMPLETE</b> flag.
          


### -param ppIPacket [out]


            Receives a pointer to the <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> interface of the first output sample of the data packet. The caller must release the interface.
          


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
</table>
 




## -remarks




        The client needs to call this method, ideally after every call to <a href="https://msdn.microsoft.com/30a693bb-255c-47a4-8102-1543872b0a5e">IMFASFMultiplexer::ProcessSample</a>, to get the output ASF packets. Call this method in a loop as long as the <b>ASF_STATUSFLAGS_INCOMPLETE</b> flag is received.
      

If no packets are ready, the method returns <b>S_OK</b> but does not return a sample in <i>ppIPacket</i>.




## -see-also




<a href="https://msdn.microsoft.com/7afa9694-c965-40e2-8549-e32ff48def2a">Generating New ASF Data Packets</a>



<a href="https://msdn.microsoft.com/bdb549b5-425b-4f77-b413-723ceb7acd11">IMFASFMultiplexer</a>



<a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a>
 

 

