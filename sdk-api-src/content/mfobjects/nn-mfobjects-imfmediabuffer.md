---
UID: NN:mfobjects.IMFMediaBuffer
title: IMFMediaBuffer (mfobjects.h)
description: Represents a block of memory that contains media data.
helpviewer_keywords: ["3ccc7089-d0d0-4eb1-b763-0d4e348af685","IMFMediaBuffer","IMFMediaBuffer interface [Media Foundation]","IMFMediaBuffer interface [Media Foundation]","described","mf.imfmediabuffer","mfobjects/IMFMediaBuffer"]
old-location: mf\imfmediabuffer.htm
tech.root: mf
ms.assetid: 3ccc7089-d0d0-4eb1-b763-0d4e348af685
ms.date: 12/05/2018
ms.keywords: 3ccc7089-d0d0-4eb1-b763-0d4e348af685, IMFMediaBuffer, IMFMediaBuffer interface [Media Foundation], IMFMediaBuffer interface [Media Foundation],described, mf.imfmediabuffer, mfobjects/IMFMediaBuffer
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
 - IMFMediaBuffer
 - mfobjects/IMFMediaBuffer
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
 - IMFMediaBuffer
---

# IMFMediaBuffer interface


## -description

Represents a block of memory that contains media data. Use this interface to access the data in the buffer.

## -inheritance

The <b>IMFMediaBuffer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaBuffer</b> also has these types of members:

## -remarks

If the buffer contains 2-D image data (such as an uncompressed video frame), you should query the buffer for the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a> interface. The methods on <b>IMF2DBuffer</b> are optimized for 2-D data.

To get a buffer from a media sample, call one of the following <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> methods:

<ul>
<li>

<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer">IMFSample::ConvertToContiguousBuffer</a>


</li>
<li>

<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex">IMFSample::GetBufferByIndex</a>


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
<a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer">MFCreateMemoryBuffer</a>
</td>
<td>Creates a buffer and allocates system memory.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediabufferwrapper">MFCreateMediaBufferWrapper</a>
</td>
<td>Creates a media buffer that wraps an existing media buffer.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer">MFCreateDXSurfaceBuffer</a>
</td>
<td>Creates a buffer that manages a DirectX surface.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer">MFCreateAlignedMemoryBuffer</a>
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

<a href="/windows/desktop/medfound/media-buffers">Media Buffers</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
