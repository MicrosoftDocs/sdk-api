---
UID: NN:mfidl.IMFMediaStream
title: IMFMediaStream
author: windows-sdk-content
description: Represents one stream in a media source.
old-location: mf\imfmediastream.htm
tech.root: medfound
ms.assetid: 66d07292-3bfe-4e68-b26f-890996262b98
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 66d07292-3bfe-4e68-b26f-890996262b98, IMFMediaStream, IMFMediaStream interface [Media Foundation], IMFMediaStream interface [Media Foundation],described, mf.imfmediastream, mfidl/IMFMediaStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
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
 - IMFMediaStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaStream interface


## -description


Represents one stream in a media source.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaStream</b> interface inherits from <a href="https://msdn.microsoft.com/a37d0840-c896-43a0-b3d1-c2a6aaff1b25">IMFMediaEventGenerator</a>. <b>IMFMediaStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ffca44ca-14ae-4f93-a719-9012a8151a7a">GetMediaSource</a>
</td>
<td align="left" width="63%">
Returns a pointer to the media source that created this media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/574eacfb-3acd-4b47-9c25-3a67aae01178">GetStreamDescriptor</a>
</td>
<td align="left" width="63%">
Returns the stream descriptor for this media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05ed4de0-fe5c-4183-8f1d-55d5a27e436a">RemoteRequestSample</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://msdn.microsoft.com/3838167b-5774-47f5-9b8d-2882eaa97167">RequestSample</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3838167b-5774-47f5-9b8d-2882eaa97167">RequestSample</a>
</td>
<td align="left" width="63%">
Requests a sample from the media source.

</td>
</tr>
</table> 


## -remarks



Streams are created when a media source is started. For each stream, the media source sends an <a href="https://msdn.microsoft.com/1bc8b265-b7a1-4068-89f7-c0da03dfb874">MENewStream</a> event with a pointer to the stream's <b>IMFMediaStream</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/a37d0840-c896-43a0-b3d1-c2a6aaff1b25">IMFMediaEventGenerator</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/65132e7d-22f6-4209-bc58-f5ea86ebd514">Media Sources</a>
 

 

