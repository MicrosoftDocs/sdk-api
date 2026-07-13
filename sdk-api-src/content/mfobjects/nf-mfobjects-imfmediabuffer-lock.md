---
UID: NF:mfobjects.IMFMediaBuffer.Lock
title: IMFMediaBuffer::Lock (mfobjects.h)
description: Gives the caller access to the memory in the buffer, for reading or writing.
helpviewer_keywords: ["28ac372a-6e73-4e66-bf69-bcc244821b71","IMFMediaBuffer interface [Media Foundation]","Lock method","IMFMediaBuffer.Lock","IMFMediaBuffer::Lock","Lock","Lock method [Media Foundation]","Lock method [Media Foundation]","IMFMediaBuffer interface","mf.imfmediabuffer_lock","mfobjects/IMFMediaBuffer::Lock"]
old-location: mf\imfmediabuffer_lock.htm
tech.root: mf
ms.assetid: 28ac372a-6e73-4e66-bf69-bcc244821b71
ms.date: 12/05/2018
ms.keywords: 28ac372a-6e73-4e66-bf69-bcc244821b71, IMFMediaBuffer interface [Media Foundation],Lock method, IMFMediaBuffer.Lock, IMFMediaBuffer::Lock, Lock, Lock method [Media Foundation], Lock method [Media Foundation],IMFMediaBuffer interface, mf.imfmediabuffer_lock, mfobjects/IMFMediaBuffer::Lock
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaBuffer::Lock
 - mfobjects/IMFMediaBuffer::Lock
dev_langs:
 - c++
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
---

# IMFMediaBuffer::Lock


## -description

Gives the caller access to the memory in the buffer, for reading or writing

## -parameters

### -param ppbBuffer [out]

Receives a pointer to the start of the buffer.

### -param pcbMaxLength [out]

Receives the maximum amount of data that can be written to the buffer. This parameter can be <b>NULL</b>. The same value is returned by the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength">IMFMediaBuffer::GetMaxLength</a> method.

### -param pcbCurrentLength [out]

Receives the length of the valid data in the buffer, in bytes. This parameter can be <b>NULL</b>. The same value is returned by the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength">IMFMediaBuffer::GetCurrentLength</a> method.

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

The pointer returned in <i>ppbBuffer</i> is guaranteed to be valid, and can safely be accessed across the entire buffer for as long as the lock is held. When you are done accessing the buffer, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock">IMFMediaBuffer::Unlock</a> to unlock the buffer. You must call <b>Unlock</b> once for each call to <b>Lock</b>. After you unlock the buffer, the pointer returned in <i>ppbBuffer</i> is no longer valid, and should not be used. Generally, it is best to call <b>Lock</b> only when you need to access the buffer memory, and not earlier.

Locking the buffer does not prevent other threads from calling <b>Lock</b>, so you should not rely on this method to synchronize threads.

This method may allocate memory, but does not transfer ownership of the memory to the caller. Do not release or free the memory; the media buffer will free the memory when the media buffer is destroyed.


If you modify the contents of the buffer, update the current length by calling <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength">IMFMediaBuffer::SetCurrentLength</a>.


This method may internally allocate some memory, so if the buffer supports the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a> interface, you should use the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d">IMF2DBuffer::Lock2D</a> method to lock the buffer instead. For 2-D buffers, the **Lock2DSize** method can be more efficient than the **Lock** method, depending on the **MF2DBuffer_LockFlags** value you specify.  Calling **Lock2DSize** with **MF2DBuffer_LockFlags_Read** won’t incur a copy back when the buffer is unlocked and calling it with **MF2DBuffer_LockFlags_Write** won’t incur a copy from the internal buffer. Calling **Lock2DSize** with **LockFlags_ReadWrite**  behaves the same as **Lock** and **Lock2D** and will incur a both copy from and copy back when unlocked. The general guidance for best performance is to avoid using **IMFMediaBuffer** and **IMF2DBuffer** whenever possible and instead use **IMF2DBuffer2** with the minimum required lock flags. Note that if the buffer is locked using **Lock2D**, the **Lock** method might return MF_E_INVALIDREQUEST.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a>



<a href="/windows/desktop/medfound/media-buffers">Media Buffers</a>
