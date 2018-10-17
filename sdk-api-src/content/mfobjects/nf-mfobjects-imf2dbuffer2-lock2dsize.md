---
UID: NF:mfobjects.IMF2DBuffer2.Lock2DSize
title: IMF2DBuffer2::Lock2DSize
author: windows-sdk-content
description: Gives the caller access to the memory in the buffer.
old-location: mf\imf2dbuffer2_lock2dsize.htm
tech.root: medfound
ms.assetid: 84885FEF-7F6D-4BE3-BF63-F9EC0C7E2D88
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: IMF2DBuffer2 interface [Media Foundation],Lock2DSize method, IMF2DBuffer2.Lock2DSize, IMF2DBuffer2::Lock2DSize, Lock2DSize, Lock2DSize method [Media Foundation], Lock2DSize method [Media Foundation],IMF2DBuffer2 interface, mf.imf2dbuffer2_lock2dsize, mfobjects/IMF2DBuffer2::Lock2DSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.h
api_name:
 - IMF2DBuffer2.Lock2DSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMF2DBuffer2::Lock2DSize


## -description


Gives the caller access to the memory in the buffer.


## -parameters




### -param lockFlags [in]

A member of the <a href="https://msdn.microsoft.com/298E3FBE-1902-4AA1-9CC8-5B8D65A48ECF">MF2DBuffer_LockFlags</a> enumeration that specifies whether to lock the buffer for reading, writing, or both.


### -param ppbScanline0 [out]

Receives a pointer to the first byte of the top row of pixels in the image. The top row is defined as the top row when the image is presented to the viewer, and might not be the first row in memory.




### -param plPitch [out]

Receives the surface stride, in bytes. The stride might be negative, indicating that the image is oriented from the bottom up in memory.




### -param ppbBufferStart [out]

Receives a pointer to the start of the accessible buffer in memory.


### -param pcbBufferLength [out]

Receives the length of the buffer, in bytes.


## -returns



This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Invalid request. The buffer might already be locked with an incompatible locking flag. See Remarks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to complete the operation. 

</td>
</tr>
</table>
 




## -remarks



When you are done accessing the memory, call <a href="https://msdn.microsoft.com/535452a3-0b38-467e-b556-80a069e4c0a5">IMF2DBuffer::Unlock2D</a> to unlock the buffer. You must call <b>Unlock2D</b> once for each call to <b>Lock2DSize</b>.

This method is equivalent to the <a href="https://msdn.microsoft.com/887a7394-9fe0-473a-825b-f095b01626c4">IMF2DBuffer::Lock2D</a> method. However, <b>Lock2DSize</b> is preferred because it enables the caller to validate memory pointers, and because it supports read-only locks. A buffer is not guaranteed to support the <a href="https://msdn.microsoft.com/BFA73B1A-F8A7-4100-9DBD-234CCA06F9F5">IMF2DBuffer2</a> interface. To access a buffer, you should try the following methods in the order listed:

<ol>
<li><b>IMF2DBuffer2::Lock2DSize</b></li>
<li>
<a href="https://msdn.microsoft.com/887a7394-9fe0-473a-825b-f095b01626c4">IMF2DBuffer::Lock2D</a>
</li>
<li>
<a href="https://msdn.microsoft.com/28ac372a-6e73-4e66-bf69-bcc244821b71">IMFMediaBuffer::Lock</a>
</li>
</ol>
The <i>ppbBufferStart</i> and <i>pcbBufferLength</i> parameters receive the bounds of the buffer memory. Use these values to guard against buffer overruns. Use the values of <i>ppbScanline0</i> and <i>plPitch</i> to access the image data. If the image is bottom-up in memory, <i>ppbScanline0</i> will point to the last scan line in memory and <i>plPitch</i> will be negative. For more information, see <a href="https://msdn.microsoft.com/13cd1106-48b3-4522-ac09-8efbaab5c31d">Image Stride</a>.

The <i>lockFlags</i> parameter specifies whether the buffer is locked for read-only access, write-only access,  or read/write access. 

<ul>
<li>If the buffer is already locked for read-only access, it cannot be locked for write access.</li>
<li>If the buffer is already locked for write-only access, it cannot be locked for read access.</li>
<li>If the buffer is already locked for read/write acess, it can be locked for read or write acess.</li>
</ul>
When possible, use a read-only or write-only lock, and avoid locking the buffer for read/write access. If the buffer represents a DirectX Graphics Infrastructure (DXGI) surface, a read/write lock can cause an extra copy between CPU memory and GPU memory.




## -see-also




<a href="https://msdn.microsoft.com/BFA73B1A-F8A7-4100-9DBD-234CCA06F9F5">IMF2DBuffer2</a>
 

 

