---
UID: NN:mfobjects.IMFMediaBuffer
title: IMFMediaBuffer (mfobjects.h)
author: windows-sdk-content
description: Represents a block of memory that contains media data.
old-location: mf\imfmediabuffer.htm
tech.root: medfound
ms.assetid: 3ccc7089-d0d0-4eb1-b763-0d4e348af685
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 3ccc7089-d0d0-4eb1-b763-0d4e348af685, IMFMediaBuffer, IMFMediaBuffer interface [Media Foundation], IMFMediaBuffer interface [Media Foundation],described, mf.imfmediabuffer, mfobjects/IMFMediaBuffer
ms.topic: interface
f1_keywords: 
 - "mfobjects/IMFMediaBuffer"
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
 - IMFMediaBuffer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaBuffer interface


## -description


Represents a block of memory that contains media data. Use this interface to access the data in the buffer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaBuffer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaBuffer</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength">GetCurrentLength</a>
</td>
<td align="left" width="63%">
Retrieves the length of the valid data in the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength">GetMaxLength</a>
</td>
<td align="left" width="63%">
Retrieves the allocated size of the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock">Lock</a>
</td>
<td align="left" width="63%">
Gives the caller access to the memory in the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength">SetCurrentLength</a>
</td>
<td align="left" width="63%">
Sets the length of the valid data in the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock">Unlock</a>
</td>
<td align="left" width="63%">
Unlocks a buffer that was previously locked.

</td>
</tr>
</table> 


## -remarks



If the buffer contains 2-D image data (such as an uncompressed video frame), you should query the buffer for the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a> interface. The methods on <b>IMF2DBuffer</b> are optimized for 2-D data.

To get a buffer from a media sample, call one of the following <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> methods:

<ul>
<li>

<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer">IMFSample::ConvertToContiguousBuffer</a>


</li>
<li>

<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex">IMFSample::GetBufferByIndex</a>


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
<a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer">MFCreateMemoryBuffer</a>
</td>
<td>Creates a buffer and allocates system memory.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediabufferwrapper">MFCreateMediaBufferWrapper</a>
</td>
<td>Creates a media buffer that wraps an existing media buffer.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer">MFCreateDXSurfaceBuffer</a>
</td>
<td>Creates a buffer that manages a DirectX surface.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer">MFCreateAlignedMemoryBuffer</a>
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




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-buffers">Media Buffers</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

