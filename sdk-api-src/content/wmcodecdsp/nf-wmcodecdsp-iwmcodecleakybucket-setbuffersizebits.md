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

# IWMCodecLeakyBucket::SetBufferSizeBits


## -description



Sets the buffer size in bits.



## -parameters




### -param ulBufferSize [in]

The buffer size, in bits.


## -returns



This method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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



This method is not implemented on the audio encoder objects. If you call this method from the <a href="https://msdn.microsoft.com/93a0169e-39fe-4152-8698-72a0650be41a">IWMCodecLeakyBucket</a> interface it returns E_NOTIMPL.

The buffer size is equal to the bit rate of the stream multiplied by the buffer window. For example, a stream with a bit rate of 28 kilobits per second with a buffer window of 3 seconds would have a buffer of 28000 bits per second x 3 seconds = 84000 bits.

This method is an alternative to setting the MFPKEY_VIDEOWINDOW property. Using this method does not alter the bit rate of the stream, but does alter the buffer window. Using the stream with a bit rate of 28000 bits per second from the previous example, setting the buffer size to 84000 using this method would have exactly the same effect as setting <a href="https://msdn.microsoft.com/da959bef-1e87-4638-9a77-4135c31a3d27">MFPKEY_VIDEOWINDOW</a> to 3000 milliseconds (3 seconds).




## -see-also




<a href="https://msdn.microsoft.com/93a0169e-39fe-4152-8698-72a0650be41a">IWMCodecLeakyBucket Interface</a>



<a href="https://msdn.microsoft.com/7fa0835e-7386-4032-a94b-ef52259aeea9">IWMCodecLeakyBucket::GetBufferSizeBits</a>
 

 

