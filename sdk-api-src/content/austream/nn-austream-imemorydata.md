---
UID: NN:austream.IMemoryData
title: IMemoryData (austream.h)
author: windows-sdk-content
description: Note  This interface is deprecated.
old-location: dshow\imemorydata.htm
tech.root: DirectShow
ms.assetid: 0e809ae7-381c-4ada-8940-5d42bf5c03da
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMemoryData, IMemoryData interface [DirectShow], IMemoryData interface [DirectShow],described, IMemoryDataInterface, austream/IMemoryData, dshow.imemorydata
ms.topic: interface
req.header: austream.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - austream.h
api_name:
 - IMemoryData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMemoryData interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IMemoryData</code> interface contains methods that set and retrieve memory data on audio data objects. Audio data objects provide the underlying data which stream samples access. This interface provides a way to initialize memory buffers and to set actual amounts of audio data in the objects. Additionally, the <a href="https://docs.microsoft.com/windows/desktop/api/austream/nf-austream-imemorydata-getinfo">GetInfo</a> method can be used to retrieve audio memory data.

Implement this interface on underlying audio data objects that audio stream sample objects will access.

Typically these methods are called by the <a href="https://docs.microsoft.com/windows/desktop/api/austream/nn-austream-iaudiomediastream">IAudioMediaStream</a> or <a href="https://docs.microsoft.com/windows/desktop/api/austream/nn-austream-iaudiostreamsample">IAudioStreamSample</a> object, rather than by the application.

In addition to the methods inherited from <b>IUnknown</b>, the <code>IMemoryData</code> interface exposes the following methods.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMemoryData</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMemoryData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMemoryData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/austream/nf-austream-imemorydata-getinfo">GetInfo</a>
</td>
<td align="left" width="63%">
Retrieves information describing an audio data object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/austream/nf-austream-imemorydata-setactual">SetActual</a>
</td>
<td align="left" width="63%">
Sets the amount of audio data currently in the object, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/austream/nf-austream-imemorydata-setbuffer">SetBuffer</a>
</td>
<td align="left" width="63%">
Initializes a memory buffer with a pointer to memory and length.

</td>
</tr>
</table> 

