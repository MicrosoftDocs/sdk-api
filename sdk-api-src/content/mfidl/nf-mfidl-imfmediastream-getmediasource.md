---
UID: NF:mfidl.IMFMediaStream.GetMediaSource
title: IMFMediaStream::GetMediaSource
author: windows-sdk-content
description: Retrieves a pointer to the media source that created this media stream.
old-location: mf\imfmediastream_getmediasource.htm
tech.root: medfound
ms.assetid: ffca44ca-14ae-4f93-a719-9012a8151a7a
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetMediaSource, GetMediaSource method [Media Foundation], GetMediaSource method [Media Foundation],IMFMediaStream interface, IMFMediaStream interface [Media Foundation],GetMediaSource method, IMFMediaStream.GetMediaSource, IMFMediaStream::GetMediaSource, ffca44ca-14ae-4f93-a719-9012a8151a7a, mf.imfmediastream_getmediasource, mfidl/IMFMediaStream::GetMediaSource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMFMediaStream.GetMediaSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaStream::GetMediaSource


## -description



Retrieves a pointer to the media source that created this media stream.




## -parameters




### -param ppMediaSource [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a> interface of the media source. The caller must release the interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media source's <a href="https://msdn.microsoft.com/c7f890a8-74bd-4418-bb02-a3fee62dec6d">Shutdown</a> method has been called.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/66d07292-3bfe-4e68-b26f-890996262b98">IMFMediaStream</a>



<a href="https://msdn.microsoft.com/65132e7d-22f6-4209-bc58-f5ea86ebd514">Media Sources</a>
 

 

