---
UID: NF:mfobjects.IMF2DBuffer.Lock2D
title: IMF2DBuffer::Lock2D
author: windows-sdk-content
description: Gives the caller access to the memory in the buffer.
old-location: mf\imf2dbuffer_lock2d.htm
old-project: medfound
ms.assetid: 887a7394-9fe0-473a-825b-f095b01626c4
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 887a7394-9fe0-473a-825b-f095b01626c4, IMF2DBuffer interface [Media Foundation],Lock2D method, IMF2DBuffer.Lock2D, IMF2DBuffer::Lock2D, Lock2D, Lock2D method [Media Foundation], Lock2D method [Media Foundation],IMF2DBuffer interface, mf.imf2dbuffer_lock2d, mfobjects/IMF2DBuffer::Lock2D
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MF_FILE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMF2DBuffer.Lock2D
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

