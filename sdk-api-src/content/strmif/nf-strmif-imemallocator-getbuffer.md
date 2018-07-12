---
UID: NF:strmif.IMemAllocator.GetBuffer
title: IMemAllocator::GetBuffer
author: windows-sdk-content
description: The GetBuffer method retrieves a media sample that contains an empty buffer.
old-location: dshow\imemallocator_getbuffer.htm
old-project: DirectShow
ms.assetid: a5d015c8-ef15-4bac-906f-5d064fbff11f
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: GetBuffer, GetBuffer method [DirectShow], GetBuffer method [DirectShow],IMemAllocator interface, IMemAllocator interface [DirectShow],GetBuffer method, IMemAllocator.GetBuffer, IMemAllocator::GetBuffer, IMemAllocatorGetBuffer, dshow.imemallocator_getbuffer, strmif/IMemAllocator::GetBuffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMemAllocator.GetBuffer
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMemAllocator::GetBuffer


## -description



The <b>GetBuffer</b> method retrieves a media sample that contains an empty buffer.




## -parameters




### -param ppBuffer [out]


            Receives a pointer to the buffer's <a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample</a> interface. The caller must release the interface.
          


### -param pStartTime [in]


            Pointer to the start time of the sample, or <b>NULL</b>.
          


### -param pEndTime [in]


            Pointer to the ending time of the sample, or <b>NULL</b>.
          


### -param dwFlags [in]

Bitwise combination of zero or more of the following flags:

<table>
<tr>
<th>
                  Flag
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>AM_GBF_NOTASYNCPOINT</td>
<td>This sample is not a synchronization point. Dynamic format changes are not allowed on this sample. When called on the Overlay Mixer or VMR, this flag implies that the buffer returned will contain an image that is identical to the last image delivered.</td>
</tr>
<tr>
<td>AM_GBF_PREVFRAMESKIPPED</td>
<td>This sample is the first after a discontinuity. (Only the video renderer uses this flag.)</td>
</tr>
<tr>
<td>AM_GBF_NOWAIT</td>
<td>Do not wait for a buffer to become available.</td>
</tr>
<tr>
<td>AM_GBF_NODDSURFACELOCK</td>
<td>Used with the <a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a> to request an unlocked DirectDraw surface. For more information, see <a href="https://msdn.microsoft.com/271b919c-421b-4484-8e60-afbf3cbdca44">Working with Direct3D Render Targets</a>.</td>
</tr>
</table>
 


## -returns



Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

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
<dt><b>VFW_E_NOT_COMMITTED</b></dt>
</dl>
</td>
<td width="60%">
Allocator is decommitted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
Timed out.

</td>
</tr>
</table>
 




## -remarks



By default, this method blocks until a free sample is available or the allocator is decommitted. If the caller specifies the AM_GBF_NOWAIT flag and no sample is available, the allocator can return immediately with a return value of VFW_E_TIMEOUT. However, allocators are not required to support this flag.

The sample returned in <i>ppBuffer</i> has a valid buffer pointer. The caller is responsible for setting any other properties on the sample, such as the time stamps, the media times, or the sync-point property. (For more information, see <a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample</a>.)

The <i>pStartTime</i> and <i>pEndTime</i> parameters are not applied to the sample. The allocator might use these values to determine which buffer it retrieves. For example, the <a href="https://msdn.microsoft.com/7719ed9d-e3b9-4c84-b587-4e120b5cabf8">Video Renderer</a> filter uses these values to synchronize switching between DirectDraw surfaces. To set the time stamp on the sample, call the <a href="https://msdn.microsoft.com/531eef13-8b04-48d2-9070-7f6e34cacd9e">IMediaSample::SetTime</a> method.

You must call the <a href="https://msdn.microsoft.com/34db4c1f-5642-4495-a572-9a78b1ee7b7e">IMemAllocator::Commit</a> method before calling this method. This method fails after the <a href="https://msdn.microsoft.com/2c1211c1-e047-4240-b85a-9be0a9290d31">IMemAllocator::Decommit</a> method is called. 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/77a161c4-706c-4270-a343-9e16c03cd590">IMemAllocator Interface</a>
 

 

