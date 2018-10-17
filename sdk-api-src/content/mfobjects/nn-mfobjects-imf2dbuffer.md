---
UID: NN:mfobjects.IMF2DBuffer
title: IMF2DBuffer
author: windows-sdk-content
description: Represents a buffer that contains a two-dimensional surface, such as a video frame.
old-location: mf\imf2dbuffer.htm
tech.root: medfound
ms.assetid: 80eb23db-a7c0-4dbe-97d8-0dc07a34d8f7
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: 80eb23db-a7c0-4dbe-97d8-0dc07a34d8f7, IMF2DBuffer, IMF2DBuffer interface [Media Foundation], IMF2DBuffer interface [Media Foundation],described, mf.imf2dbuffer, mfobjects/IMF2DBuffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IMF2DBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMF2DBuffer interface


## -description


Represents a buffer that contains a two-dimensional surface, such as a video frame.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMF2DBuffer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMF2DBuffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMF2DBuffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84634782-7805-4e2b-a043-7e49adef5c2a">ContiguousCopyFrom</a>
</td>
<td align="left" width="63%">
Copies data to this buffer from a buffer that has a contiguous format.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32601f2e-ab91-4a65-bcf4-8e063e90fbb0">ContiguousCopyTo</a>
</td>
<td align="left" width="63%">
Copies this buffer into the caller's buffer, converting the data to contiguous format.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/413d50f6-a047-4561-985d-9d1927825617">GetContiguousLength</a>
</td>
<td align="left" width="63%">
Retrieves the number of bytes needed to store the contents of the buffer in contiguous format.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08a5f659-609d-4a86-a24e-b30bb7f9e835">GetScanline0AndPitch</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the buffer memory and the surface stride.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2042d1f-4d80-4dfd-b57e-33f6a6d07d6e">IsContiguousFormat</a>
</td>
<td align="left" width="63%">
Queries whether the buffer is contiguous in its native format.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/887a7394-9fe0-473a-825b-f095b01626c4">Lock2D</a>
</td>
<td align="left" width="63%">
Gives the caller access to the memory in the buffer.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/535452a3-0b38-467e-b556-80a069e4c0a5">Unlock2D</a>
</td>
<td align="left" width="63%">
Unlocks a buffer that was previously locked.
        

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <b>QueryInterface</b> on the media buffer.

To use a 2-D buffer, it is important to know the <i>stride</i>, which is the number of bytes needed to go from one row of pixels to the next. The stride may be larger than the image width, because the surface may contain padding bytes after each row of pixels. Stride can also be negative, if the pixels are oriented bottom-up in memory. For more information, see <a href="https://msdn.microsoft.com/13cd1106-48b3-4522-ac09-8efbaab5c31d">Image Stride</a>.

Every video format defines a <i>contiguous</i> or <i>packed</i> representation. This representation is compatible with the standard layout of a DirectX surface in system memory, with no additional padding. For RGB video, the contiguous representation has a pitch equal to the image width in bytes, rounded up to the nearest <b>DWORD</b> boundary. For YUV video, the layout of the contiguous representation depends on the YUV format. For planar YUV formats, the Y plane might have a different pitch than the U and V planes.

If a media buffer supports the <b>IMF2DBuffer</b> interface, the underlying buffer is not guaranteed to have a contiguous representation, because there might be additional padding bytes after each row of pixels. When a buffer is non-contiguous, the <a href="https://msdn.microsoft.com/28ac372a-6e73-4e66-bf69-bcc244821b71">Lock</a> and <a href="https://msdn.microsoft.com/887a7394-9fe0-473a-825b-f095b01626c4">Lock2D</a> methods have different behaviors:

<ul>
<li>The <a href="https://msdn.microsoft.com/887a7394-9fe0-473a-825b-f095b01626c4">Lock2D</a> method returns a pointer to the underlying buffer. The buffer might not be contiguous.
          </li>
<li>The <a href="https://msdn.microsoft.com/28ac372a-6e73-4e66-bf69-bcc244821b71">Lock</a> method returns a buffer that is guaranteed to be contiguous. If the underlying buffer is not contiguous, the method copies the data into a new buffer, and the <a href="https://msdn.microsoft.com/3ca53321-5533-45f0-b415-6a16f780ec54">Unlock</a> method copies it back into the original buffer.
          </li>
</ul>
Call the <a href="https://msdn.microsoft.com/887a7394-9fe0-473a-825b-f095b01626c4">Lock2D</a> method to access the 2-D buffer in its native format. The native format might not be contiguous. The buffer's <a href="https://msdn.microsoft.com/28ac372a-6e73-4e66-bf69-bcc244821b71">IMFMediaBuffer::Lock</a> method returns a contiguous representation of the buffer. However, this might require an internal copy from the native format. For 2-D buffers, therefore, you should use the <b>Lock2D</b> method and avoid the <b>Lock</b> method. Because the <b>Lock</b> method might cause up to two buffer copies, the <b>Lock2D</b> method is generally more efficient and should be used when possible. To find out if the underlying buffer is contiguous, call <a href="https://msdn.microsoft.com/a2042d1f-4d80-4dfd-b57e-33f6a6d07d6e">IMF2DBuffer::IsContiguousFormat</a>.

For uncompressed images, the amount of valid data in the buffer is determined by the width, height, and pixel layout of the image. For this reason, if you call <a href="https://msdn.microsoft.com/887a7394-9fe0-473a-825b-f095b01626c4">Lock2D</a> to access the buffer, do not rely on the values returned by <a href="https://msdn.microsoft.com/772e3e6c-0616-41f6-a681-d76da97d85fb">IMFMediaBuffer::GetCurrentLength</a> or <a href="https://msdn.microsoft.com/f0697f1d-18d6-4406-9f19-8cbaac08ad47">IMFMediaBuffer::GetMaxLength</a>. Similarly, if you modify the data in the buffer, you do not have to call <a href="https://msdn.microsoft.com/ce48458f-eb0f-441a-a4bc-9d3fbee0cd74">IMFMediaBuffer::SetCurrentLength</a> to update the size. Generally, you should avoid mixing calls to <b>IMF2DBuffer</b> and <a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a> methods on the same media buffer.




## -see-also




<a href="https://msdn.microsoft.com/3ee073ea-7bac-4971-9167-93a4e541ab77">Media Buffers</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/be5ec8a8-2d0b-401b-9d05-fdb87ad8c864">Uncompressed Video Buffers</a>
 

 

