---
UID: NN:mfobjects.IMFMediaBuffer
title: IMFMediaBuffer
author: windows-sdk-content
description: Represents a block of memory that contains media data.
old-location: mf\imfmediabuffer.htm
old-project: medfound
ms.assetid: 3ccc7089-d0d0-4eb1-b763-0d4e348af685
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: 3ccc7089-d0d0-4eb1-b763-0d4e348af685, IMFMediaBuffer, IMFMediaBuffer interface [Media Foundation], IMFMediaBuffer interface [Media Foundation],described, mf.imfmediabuffer, mfobjects/IMFMediaBuffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaBuffer
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaBuffer interface


## -description


Represents a block of memory that contains media data. Use this interface to access the data in the buffer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaBuffer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaBuffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaBuffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/772e3e6c-0616-41f6-a681-d76da97d85fb">GetCurrentLength</a>
</td>
<td align="left" width="63%">
Retrieves the length of the valid data in the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0697f1d-18d6-4406-9f19-8cbaac08ad47">GetMaxLength</a>
</td>
<td align="left" width="63%">
Retrieves the allocated size of the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28ac372a-6e73-4e66-bf69-bcc244821b71">Lock</a>
</td>
<td align="left" width="63%">
Gives the caller access to the memory in the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce48458f-eb0f-441a-a4bc-9d3fbee0cd74">SetCurrentLength</a>
</td>
<td align="left" width="63%">
Sets the length of the valid data in the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ca53321-5533-45f0-b415-6a16f780ec54">Unlock</a>
</td>
<td align="left" width="63%">
Unlocks a buffer that was previously locked.

</td>
</tr>
</table> 


## -remarks



If the buffer contains 2-D image data (such as an uncompressed video frame), you should query the buffer for the <a href="https://msdn.microsoft.com/80eb23db-a7c0-4dbe-97d8-0dc07a34d8f7">IMF2DBuffer</a> interface. The methods on <b>IMF2DBuffer</b> are optimized for 2-D data.

To get a buffer from a media sample, call one of the following <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> methods:

<ul>
<li>

<a href="https://msdn.microsoft.com/6ea950eb-7f2e-4549-93dc-fa62f95b7b66">IMFSample::ConvertToContiguousBuffer</a>


</li>
<li>

<a href="https://msdn.microsoft.com/48d3b861-96e8-4767-a8b1-65614fd48254">IMFSample::GetBufferByIndex</a>


</li>
</ul>
To create a new buffer object, use one of the following functions.

<table>
<tr>
<th>Function</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/1f79d057-7ef7-4662-9f82-ceadc23276f0">MFCreateMemoryBuffer</a>
</td>
<td>Creates a buffer and allocates system memory.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/6850e75c-4612-4514-a74d-9b36fd88a598">MFCreateMediaBufferWrapper</a>
</td>
<td>Creates a media buffer that wraps an existing media buffer.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/d1ee158e-5d70-41a4-b746-2ecaea2db92c">MFCreateDXSurfaceBuffer</a>
</td>
<td>Creates a buffer that manages a DirectX surface.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/cccc0dea-3f1e-41e4-97f4-de7760ceccb0">MFCreateAlignedMemoryBuffer</a>
</td>
<td>Creates a buffer and allocates system memory with a specified alignment.</td>
</tr>
</table>
 

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3ee073ea-7bac-4971-9167-93a4e541ab77">Media Buffers</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

