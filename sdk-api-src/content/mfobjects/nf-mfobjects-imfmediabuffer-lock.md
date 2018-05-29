---
UID: NF:mfobjects.IMFMediaBuffer.Lock
title: IMFMediaBuffer::Lock
author: windows-sdk-content
description: Gives the caller access to the memory in the buffer, for reading or writing.
old-location: mf\imfmediabuffer_lock.htm
old-project: medfound
ms.assetid: 28ac372a-6e73-4e66-bf69-bcc244821b71
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 28ac372a-6e73-4e66-bf69-bcc244821b71, IMFMediaBuffer interface [Media Foundation],Lock method, IMFMediaBuffer.Lock, IMFMediaBuffer::Lock, Lock, Lock method [Media Foundation], Lock method [Media Foundation],IMFMediaBuffer interface, mf.imfmediabuffer_lock, mfobjects/IMFMediaBuffer::Lock
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
-	IMFMediaBuffer.Lock
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaBuffer::Lock


## -description



Gives the caller access to the memory in the buffer, for reading or writing




## -parameters




### -param ppbBuffer [out]

Receives a pointer to the start of the buffer.


### -param pcbMaxLength [out]

Receives the maximum amount of data that can be written to the buffer. This parameter can be <b>NULL</b>. The same value is returned by the <a href="https://msdn.microsoft.com/f0697f1d-18d6-4406-9f19-8cbaac08ad47">IMFMediaBuffer::GetMaxLength</a> method.


### -param pcbCurrentLength [out]

Receives the length of the valid data in the buffer, in bytes. This parameter can be <b>NULL</b>. The same value is returned by the <a href="https://msdn.microsoft.com/772e3e6c-0616-41f6-a681-d76da97d85fb">IMFMediaBuffer::GetCurrentLength</a> method.


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
For Direct3D surface buffers, an error occurred when locking the surface.

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



This method gives the caller access to the entire buffer, up to the maximum size returned in the <i>pcbMaxLength</i> parameter. The value returned in <i>pcbCurrentLength</i> is the size of any valid data already in the buffer, which might be less than the total buffer size.

The pointer returned in <i>ppbBuffer</i> is guaranteed to be valid, and can safely be accessed across the entire buffer for as long as the lock is held. When you are done accessing the buffer, call <a href="https://msdn.microsoft.com/3ca53321-5533-45f0-b415-6a16f780ec54">IMFMediaBuffer::Unlock</a> to unlock the buffer. You must call <b>Unlock</b> once for each call to <b>Lock</b>. After you unlock the buffer, the pointer returned in <i>ppbBuffer</i> is no longer valid, and should not be used. Generally, it is best to call <b>Lock</b> only when you need to access the buffer memory, and not earlier.

Locking the buffer does not prevent other threads from calling <b>Lock</b>, so you should not rely on this method to synchronize threads.

This method does not allocate any memory, or transfer ownership of the memory to the caller. Do not release or free the memory; the media buffer will free the memory when the media buffer is destroyed.

If you modify the contents of the buffer, update the current length by calling <a href="https://msdn.microsoft.com/ce48458f-eb0f-441a-a4bc-9d3fbee0cd74">IMFMediaBuffer::SetCurrentLength</a>.

If the buffer supports the <a href="https://msdn.microsoft.com/80eb23db-a7c0-4dbe-97d8-0dc07a34d8f7">IMF2DBuffer</a> interface, you should use the <a href="https://msdn.microsoft.com/887a7394-9fe0-473a-825b-f095b01626c4">IMF2DBuffer::Lock2D</a> method to lock the buffer. For 2-D buffers, the <b>Lock2D</b> method is more efficient than the <b>Lock</b> method. If the buffer is locked using <b>Lock2D</b>, the Lock method might return <b>MF_E_INVALIDREQUEST</b>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a>



<a href="https://msdn.microsoft.com/3ee073ea-7bac-4971-9167-93a4e541ab77">Media Buffers</a>
 

 

