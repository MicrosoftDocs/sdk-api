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

# IStreamConcatenate::Append2


## -description


Appends an array of streams to this stream.


## -parameters




### -param streams [in]

Array of  <b>IStream</b> interfaces of the streams to append to this stream.


### -param streamCount [in]

Number of streams in <i>streams</i>.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

Value: 0x80004001

</td>
</tr>
</table>
 




## -remarks



You must call the <a href="https://msdn.microsoft.com/62db148e-926d-47b3-a0f6-945730177184">IStreamConcatenate::Initialize</a> or <a href="https://msdn.microsoft.com/826b3157-4cab-4f18-87f2-6635911c03f0">IStreamConcatenate::Initialize2</a> method prior to calling this method.

To append a single stream to this stream, call the <a href="https://msdn.microsoft.com/9871cc35-c955-4fd4-9082-5b6ab60cae7b">IStreamConcatenate::Append</a> method.




## -see-also




<a href="https://msdn.microsoft.com/48b786ef-a1b6-4dcf-9329-c659f15185e1">IStreamConcatenate</a>



<a href="https://msdn.microsoft.com/9871cc35-c955-4fd4-9082-5b6ab60cae7b">IStreamConcatenate::Append</a>
 

 

