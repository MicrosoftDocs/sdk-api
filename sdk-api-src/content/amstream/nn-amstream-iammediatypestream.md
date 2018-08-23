---
UID: NN:amstream.IAMMediaTypeStream
title: IAMMediaTypeStream
author: windows-sdk-content
description: Note  This interface is deprecated.
old-location: dshow\iammediatypestream.htm
old-project: DirectShow
ms.assetid: 6ca1bad2-625b-4415-8311-acd5443452c1
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IAMMediaTypeStream, IAMMediaTypeStream interface [DirectShow], IAMMediaTypeStream interface [DirectShow],described, IAMMediaTypeStreamInterface, amstream/IAMMediaTypeStream, dshow.iammediatypestream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: amstream.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: AMSI_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMediaTypeStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAMMediaTypeStream interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
This interface contains methods for creating multimedia streams with arbitrary media types. Use this interface if you need to create a multimedia stream with a format that is not supported by the other Microsoft DirectShow multimedia streaming interfaces.

<div class="alert"><b>Note</b>  For video streams, use the <a href="https://msdn.microsoft.com/858af0c3-9e22-45d8-ab08-307eb39a8977">IDirectDrawMediaStream</a> interface instead of this interface. For audio streams, use the <a href="https://msdn.microsoft.com/b4098876-6c11-4cc6-8b6d-16edc02316f3">IAudioMediaStream</a> interface.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMMediaTypeStream</b> interface inherits from <a href="https://msdn.microsoft.com/97f5dfdc-5941-4b58-a618-1c7e9f6665e1">IMediaStream</a>. <b>IAMMediaTypeStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMMediaTypeStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5bfdbf82-c298-498d-84e4-cd4d8cd13f82">CreateSample</a>
</td>
<td align="left" width="63%">
Creates a stream sample and optionally specifies the sample buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f00fe45-df4b-4787-980c-9fe434a8ab7e">GetFormat</a>
</td>
<td align="left" width="63%">
Retrieves the format of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a1ad5c5-0cbf-44a5-833f-951c9934bd19">GetStreamAllocatorRequirements</a>
</td>
<td align="left" width="63%">
Retrieves the allocator requirements for the stream. This method is not currently implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12ac4490-c12c-428a-939f-adf25a77b9e4">SetFormat</a>
</td>
<td align="left" width="63%">
Sets the format of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d34a00dd-e863-4356-97f9-da3776ecb47b">SetStreamAllocatorRequirements</a>
</td>
<td align="left" width="63%">
Sets the allocator requirements for the stream. This method is not currently implemented.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/97f5dfdc-5941-4b58-a618-1c7e9f6665e1">IMediaStream</a>
 

 

