---
UID: NN:mfidl.IMFMediaSource
title: IMFMediaSource
author: windows-sdk-content
description: Implemented by media source objects.
old-location: mf\imfmediasource.htm
old-project: medfound
ms.assetid: 8b579f61-6fea-4b20-a051-7633fc01fa05
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 8b579f61-6fea-4b20-a051-7633fc01fa05, IMFMediaSource, IMFMediaSource interface [Media Foundation], IMFMediaSource interface [Media Foundation],described, mf.imfmediasource, mfidl/IMFMediaSource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
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
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFMediaSource
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaSource interface


## -description


Implemented by media source objects.

Media sources are objects that generate media data. For example, the data might come from a video file, a network stream, or a hardware device, such as a camera. Each media source contains one or more streams, and each stream delivers data of one type, such as audio or video.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaSource</b> interface inherits from <a href="https://msdn.microsoft.com/a37d0840-c896-43a0-b3d1-c2a6aaff1b25">IMFMediaEventGenerator</a>. <b>IMFMediaSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaSource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6ac50b7-3ef1-43cf-8126-d9a003ebd825">CreatePresentationDescriptor</a>
</td>
<td align="left" width="63%">
Retrieves a copy of the media source's presentation descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb5d54cd-58a3-4903-b22e-8207f90dbbc0">GetCharacteristics</a>
</td>
<td align="left" width="63%">
Retrieves the characteristics of the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451189">Pause</a>
</td>
<td align="left" width="63%">
Pauses all active streams in the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ad6793e-32ca-471b-8639-41098b3e8216">RemoteCreatePresentationDescriptor</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://msdn.microsoft.com/b6ac50b7-3ef1-43cf-8126-d9a003ebd825">CreatePresentationDescriptor</a>. (Not used by applications.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a>
</td>
<td align="left" width="63%">
Shuts down the media source and releases the resources it is using.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a>
</td>
<td align="left" width="63%">
Starts, seeks, or restarts the media source by specifying where to start playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a>
</td>
<td align="left" width="63%">
Stops all active streams in the media source.

</td>
</tr>
</table> 


## -remarks



In Windows 8, this interface is extended with <a href="https://msdn.microsoft.com/C72C79D5-FD65-4F27-A8C8-B94BF5A9E829">IMFMediaSourceEx</a>.




## -see-also




<a href="https://msdn.microsoft.com/a37d0840-c896-43a0-b3d1-c2a6aaff1b25">IMFMediaEventGenerator</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/65132e7d-22f6-4209-bc58-f5ea86ebd514">Media Sources</a>
 

 

