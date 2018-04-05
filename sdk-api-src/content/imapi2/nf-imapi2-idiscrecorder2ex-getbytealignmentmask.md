---
UID: NF:imapi2.IDiscRecorder2Ex.GetByteAlignmentMask
title: IDiscRecorder2Ex::GetByteAlignmentMask method
author: windows-driver-content
description: Retrieves the byte alignment mask for the device.
old-location: imapi\idiscrecorder2ex_getbytealignmentmask.htm
old-project: imapi
ms.assetid: 6a92efb1-4da8-4cf4-8011-b06a0f82a3eb
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetByteAlignmentMask method [IMAPI], GetByteAlignmentMask method [IMAPI], IDiscRecorder2Ex interface, GetByteAlignmentMask,IDiscRecorder2Ex.GetByteAlignmentMask, IDiscRecorder2Ex, IDiscRecorder2Ex interface [IMAPI], GetByteAlignmentMask method, IDiscRecorder2Ex::GetByteAlignmentMask, imapi.idiscrecorder2ex_getbytealignmentmask, imapi2/IDiscRecorder2Ex::GetByteAlignmentMask
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2.h
api_name:
-	IDiscRecorder2Ex.GetByteAlignmentMask
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscRecorder2Ex::GetByteAlignmentMask method


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
 

 

