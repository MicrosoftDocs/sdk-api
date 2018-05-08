---
UID: NN:mfobjects.IMFSample
title: IMFSample
author: windows-driver-content
description: Represents a media sample, which is a container object for media data.
old-location: mf\imfsample.htm
old-project: medfound
ms.assetid: b1c3758c-5133-41ee-b991-ae99d0296ccc
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: IMFSample, IMFSample interface [Media Foundation], IMFSample interface [Media Foundation],described, b1c3758c-5133-41ee-b991-ae99d0296ccc, mf.imfsample, mfobjects/IMFSample
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IMFSample
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFSample interface


## -description


Represents a media sample, which is a container object for media data. For video, a sample typically contains one video frame. For audio data, a sample typically contains multiple audio samples, rather than a single sample of audio.

A media sample contains zero or more buffers. Each buffer manages a block of memory, and is represented by the <a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a> interface. A sample can have multiple buffers. The buffers are kept in an ordered list and accessed by index value. It is also valid to have an empty sample with no buffers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSample</b> interface inherits from <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>. <b>IMFSample</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSample</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983406">AddBuffer</a>
</td>
<td align="left" width="63%">
Adds a buffer to the end of the list of buffers in the sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ea950eb-7f2e-4549-93dc-fa62f95b7b66">ConvertToContiguousBuffer</a>
</td>
<td align="left" width="63%">
Converts a sample with multiple buffers into a sample with a single buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8a23e0a-ed2f-449d-b834-f60f383d0b5e">CopyToBuffer</a>
</td>
<td align="left" width="63%">
Copies the sample data to a buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48d3b861-96e8-4767-a8b1-65614fd48254">GetBufferByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a buffer from the sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe05e870-298b-44bf-90b7-70be40d045ab">GetBufferCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of buffers in the sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3284edc-b9b5-489b-9166-3bb6da50bd2a">GetSampleDuration</a>
</td>
<td align="left" width="63%">
Retrieves the duration of the sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98e3ed97-cefc-40c2-acda-8b3da74d0d03">GetSampleFlags</a>
</td>
<td align="left" width="63%">
Retrieves flags associated with the sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc4aac9e-e7a9-43f0-af7b-54a39666044a">GetSampleTime</a>
</td>
<td align="left" width="63%">
Retrieves the presentation time of the sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0dfc1d2-ec78-4d1c-992d-3a876b600ca6">GetTotalLength</a>
</td>
<td align="left" width="63%">
Retrieves the total length of the valid data in all of the buffers in the sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7ce734f-64da-4d45-905e-54a8898aa710">RemoveAllBuffers</a>
</td>
<td align="left" width="63%">
Removes all buffers from the sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc7b5a46-a127-4d75-a9a5-382d9d65a426">RemoveBufferByIndex</a>
</td>
<td align="left" width="63%">
Removes a buffer at a specified index from the sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f97be98e-8f1b-4bae-8cdd-8bdfe107894d">SetSampleDuration</a>
</td>
<td align="left" width="63%">
Sets the duration of the sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30dac293-981b-41f3-951d-186d6a603d0a">SetSampleFlags</a>
</td>
<td align="left" width="63%">
Sets flags associated with the sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59d32002-2f5c-4a94-bd09-fd5a2c005ffc">SetSampleTime</a>
</td>
<td align="left" width="63%">
Sets the presentation time of the sample.

</td>
</tr>
</table> 


## -remarks



To create a new media sample, call <a href="https://msdn.microsoft.com/b8bc29a5-e872-4c7b-ad1d-6c6085aa1984">MFCreateSample</a>.

<div class="alert"><b>Note</b>  <p class="note">When you call <a href="https://msdn.microsoft.com/111b55bc-fb8e-45b5-a709-703acd23c4be">CopyAllItems</a>, inherited from the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface, on an <b>IMFSample</b>, the sample time, duration, and flags are not copied to the destination sample. You must copy these values to the new sample manually.

</div>
<div> </div>
This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/14389eea-8091-4c10-849e-53db3e98a7c8">Media Samples</a>



<a href="https://msdn.microsoft.com/64aead5a-61c4-4e83-a556-af33e0aa82be">Sample Attributes</a>
 

 

