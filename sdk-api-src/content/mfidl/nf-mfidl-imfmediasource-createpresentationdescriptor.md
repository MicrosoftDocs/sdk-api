---
UID: NF:mfidl.IMFMediaSource.CreatePresentationDescriptor
title: IMFMediaSource::CreatePresentationDescriptor
author: windows-sdk-content
description: Retrieves a copy of the media source's presentation descriptor. Applications use the presentation descriptor to select streams and to get information about the source content.
old-location: mf\imfmediasource_createpresentationdescriptor.htm
tech.root: medfound
ms.assetid: b6ac50b7-3ef1-43cf-8126-d9a003ebd825
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: CreatePresentationDescriptor, CreatePresentationDescriptor method [Media Foundation], CreatePresentationDescriptor method [Media Foundation],IMFMediaSource interface, IMFMediaSource interface [Media Foundation],CreatePresentationDescriptor method, IMFMediaSource.CreatePresentationDescriptor, IMFMediaSource::CreatePresentationDescriptor, b6ac50b7-3ef1-43cf-8126-d9a003ebd825, mf.imfmediasource_createpresentationdescriptor, mfidl/IMFMediaSource::CreatePresentationDescriptor
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
 - IMFMediaSource.CreatePresentationDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaSource::CreatePresentationDescriptor


## -description



Retrieves a copy of the media source's presentation descriptor. Applications use the presentation descriptor to select streams and to get information about the source content.




## -parameters




### -param ppPresentationDescriptor [out]

Receives a pointer to the presentation descriptor's <a href="https://msdn.microsoft.com/db03e212-7021-433e-84dc-410b2cf7af87">IMFPresentationDescriptor</a> interface. The caller must release the interface.


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
 




## -remarks



The presentation descriptor contains the media source's default settings for the presentation. The application can change these settings by selecting or deselecting streams, or by changing the media type on a stream. Do not modify the presentation descriptor unless the source is stopped. The changes take affect when the source's <a href="https://msdn.microsoft.com/0a5abafe-1525-4bda-946c-05a6145e57ee">IMFMediaSource::Start</a> method is called.




## -see-also




<a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a>



<a href="https://msdn.microsoft.com/65132e7d-22f6-4209-bc58-f5ea86ebd514">Media Sources</a>
 

 

