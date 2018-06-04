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

# IDiscRecorder2Ex::GetByteAlignmentMask


## -description


Retrieves the byte alignment mask for the device.


## -parameters




### -param value [out]

Byte alignment mask that you use to determine if the buffer is aligned to the correct byte boundary for the device. The byte alignment value is always a number that is a power of 2.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified failure.

Value: 0x80004005

</td>
</tr>
</table>
 




## -remarks



The data buffer for <a href="https://msdn.microsoft.com/e893c3d8-1bf8-461e-9792-3b7d6d3beebb">IDiscRecorder2Ex::SendCommandSendDataToDevice</a> and <a href="https://msdn.microsoft.com/d3142b79-4e46-4cb8-ab4a-3bf5823cd26e">IDiscRecorder2Ex::SendCommandGetDataFromDevice</a> must aligned to the correct byte boundary. To determine if the buffer is on the correct byte boundary, perform a bitwise logical AND of the bitmask with  the address of the data buffer. For example, if the address of the buffer is 0x3840958, you can test for correct alignment using the following statement:

<pre class="syntax" xml:space="preserve"><code>if (0x3840958 &amp; (value - 1) == 0)
{
    // The alignment is correct
}</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/37e65b57-ec53-405c-a7bd-34c2df15d5d7">IDiscRecorder2Ex</a>



<a href="https://msdn.microsoft.com/d3142b79-4e46-4cb8-ab4a-3bf5823cd26e">IDiscRecorder2Ex::SendCommandGetDataFromDevice</a>



<a href="https://msdn.microsoft.com/7dc645d5-795d-4f31-a4cf-30875e930e10">IDiscRecorder2Ex::SendCommandNoData</a>



<a href="https://msdn.microsoft.com/e893c3d8-1bf8-461e-9792-3b7d6d3beebb">IDiscRecorder2Ex::SendCommandSendDataToDevice</a>
 

 

