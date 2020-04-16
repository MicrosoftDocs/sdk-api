---
UID: NF:mfobjects.IMFMediaBuffer.Lock
title: IMFMediaBuffer::Lock (mfobjects.h)
description: Gives the caller access to the memory in the buffer, for reading or writing.
old-location: mf\imfmediabuffer_lock.htm
tech.root: medfound
ms.assetid: 28ac372a-6e73-4e66-bf69-bcc244821b71
ms.date: 12/05/2018
ms.keywords: 28ac372a-6e73-4e66-bf69-bcc244821b71, IMFMediaBuffer interface [Media Foundation],Lock method, IMFMediaBuffer.Lock, IMFMediaBuffer::Lock, Lock, Lock method [Media Foundation], Lock method [Media Foundation],IMFMediaBuffer interface, mf.imfmediabuffer_lock, mfobjects/IMFMediaBuffer::Lock
f1_keywords:
- mfobjects/IMFMediaBuffer.Lock
dev_langs:
- c++
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFMediaBuffer.Lock
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaBuffer::Lock


## -description



Gives the caller access to the memory in the buffer, for reading or writing




## -parameters




### -param ppbBuffer [out]

Receives a pointer to the start of the buffer.


### -param pcbMaxLength [out]

Receives the maximum amount of data that can be written to the buffer. This parameter can be <b>NULL</b>. The same value is returned by the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength">IMFMediaBuffer::GetMaxLength</a> method.


### -param pcbCurrentLength [out]

Receives the length of the valid data in the buffer, in bytes. This parameter can be <b>NULL</b>. The same value is returned by the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength">IMFMediaBuffer::GetCurrentLength</a> method.


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

The pointer returned in <i>ppbBuffer</i> is guaranteed to be valid, and can safely be accessed across the entire buffer for as long as the lock is held. When you are done accessing the buffer, call <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock">IMFMediaBuffer::Unlock</a> to unlock the buffer. You must call <b>Unlock</b> once for each call to <b>Lock</b>. After you unlock the buffer, the pointer returned in <i>ppbBuffer</i> is no longer valid, and should not be used. Generally, it is best to call <b>Lock</b> only when you need to access the buffer memory, and not earlier.

Locking the buffer does not prevent other threads from calling <b>Lock</b>, so you should not rely on this method to synchronize threads.

This method does not transfer ownership of the memory to the caller. Do not release or free the memory; the media buffer will free the memory when the media buffer is destroyed.

If you modify the contents of the buffer, update the current length by calling <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength">IMFMediaBuffer::SetCurrentLength</a>.

This method may internally allocate some memory. Depending on the interfaces the buffer supports, some better alternatives might exist which reduce the chance of allocating memory. If the buffer supports the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer2">IMF2DBuffer2</a> interface, you should use the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer2-lock2dsize">IMF2DBuffer2::Lock2DSize</a> method to lock the buffer. For 2-D buffers, the <b>Lock2DSize</b> method is more efficient than the <b>Lock</b> method. If the buffer does not support the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer2">IMF2DBuffer2</a> interface but supports the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a> interface, you should use the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d">IMF2DBuffer::Lock2D</a> method to lock the buffer. For 2-D buffers, the <b>Lock2D</b> method is more efficient than the <b>Lock</b> method (but less efficient than the <b>Lock2DSize</b> method). If the buffer is locked using <b>Lock2D</b> or <b>Lock2DSize</b>, the <b>Lock</b> method might return <b>MF_E_INVALIDREQUEST</b>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also

<a href="https://docs.microsoft.com/en-us/windows/win32/api/mfobjects/nn-mfobjects-imf2dbuffer2">IMF2DBuffer2</a>

<a href="https://docs.microsoft.com/en-us/windows/win32/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a>

<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a>

<a href="https://docs.microsoft.com/windows/desktop/medfound/media-buffers">Media Buffers</a>
 

 

