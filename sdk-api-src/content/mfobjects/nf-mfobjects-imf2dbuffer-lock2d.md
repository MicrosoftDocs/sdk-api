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

# IMF2DBuffer::Lock2D


## -description



Gives the caller access to the memory in the buffer.




## -parameters




### -param ppbScanline0




### -param plPitch [out]

Receives the surface stride, in bytes. The stride might be negative, indicating that the image is oriented from the bottom up in memory.


#### - pbScanline0 [out]

Receives a pointer to the first byte of the top row of pixels in the image. The top row is defined as the top row when the image is presented to the viewer, and might not be the first row in memory.


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
<dt><b>D3DERR_INVALIDCALL</b></dt>
</dl>
</td>
<td width="60%">
Cannot lock the Direct3D surface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The buffer cannot be locked at this time.

</td>
</tr>
</table>
 




## -remarks



If <i>p</i> is a pointer to the first byte in a row of pixels, <i>p</i> + (*<i>plPitch</i>) points to the first byte in the next row of pixels. A buffer might contain padding after each row of pixels, so the stride might be wider than the width of the image in bytes. Do not access the memory that is reserved for padding bytes, because it might not be read-accessible or write-accessible. For more information, see <a href="https://msdn.microsoft.com/13cd1106-48b3-4522-ac09-8efbaab5c31d">Image Stride</a>.

The pointer returned in <i>pbScanline0</i> remains valid as long as the caller holds the lock. When you are done accessing the memory, call <a href="https://msdn.microsoft.com/535452a3-0b38-467e-b556-80a069e4c0a5">IMF2DBuffer::Unlock2D</a> to unlock the buffer. You must call <b>Unlock2D</b> once for each call to <b>Lock2D</b>. After you unlock the buffer, the pointer returned in <i>pbScanline0</i> is no longer valid and should not be used. Generally, it is best to call <b>Lock2D</b> only when you need to access the buffer memory, and not earlier.

The values returned by the <a href="https://msdn.microsoft.com/772e3e6c-0616-41f6-a681-d76da97d85fb">IMFMediaBuffer::GetCurrentLength</a> and <a href="https://msdn.microsoft.com/f0697f1d-18d6-4406-9f19-8cbaac08ad47">IMFMediaBuffer::GetMaxLength</a> methods do not apply to the buffer that is returned by the <b>Lock2D</b> method. For the same reason, you do not need to call <a href="https://msdn.microsoft.com/ce48458f-eb0f-441a-a4bc-9d3fbee0cd74">IMFMediaBuffer::SetCurrentLength</a> after manipulating the data in the buffer returned by the <b>Lock2D</b> method.

The <a href="https://msdn.microsoft.com/28ac372a-6e73-4e66-bf69-bcc244821b71">IMFMediaBuffer::Lock</a> method fails while the <b>Lock2D</b> lock is held, and vice-versa. Applications should use only one of these methods at a time.

When the underlying buffer is a Direct3D surface, the method fails if the surface is not lockable.




## -see-also




<a href="https://msdn.microsoft.com/80eb23db-a7c0-4dbe-97d8-0dc07a34d8f7">IMF2DBuffer</a>



<a href="https://msdn.microsoft.com/3ee073ea-7bac-4971-9167-93a4e541ab77">Media Buffers</a>



<a href="https://msdn.microsoft.com/be5ec8a8-2d0b-401b-9d05-fdb87ad8c864">Uncompressed Video Buffers</a>
 

 

