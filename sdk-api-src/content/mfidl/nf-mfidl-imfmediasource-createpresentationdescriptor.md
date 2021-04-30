---
UID: NF:mfidl.IMFMediaSource.CreatePresentationDescriptor
title: IMFMediaSource::CreatePresentationDescriptor (mfidl.h)
description: Retrieves a copy of the media source's presentation descriptor. Applications use the presentation descriptor to select streams and to get information about the source content.
helpviewer_keywords: ["CreatePresentationDescriptor","CreatePresentationDescriptor method [Media Foundation]","CreatePresentationDescriptor method [Media Foundation]","IMFMediaSource interface","IMFMediaSource interface [Media Foundation]","CreatePresentationDescriptor method","IMFMediaSource.CreatePresentationDescriptor","IMFMediaSource::CreatePresentationDescriptor","b6ac50b7-3ef1-43cf-8126-d9a003ebd825","mf.imfmediasource_createpresentationdescriptor","mfidl/IMFMediaSource::CreatePresentationDescriptor"]
old-location: mf\imfmediasource_createpresentationdescriptor.htm
tech.root: mf
ms.assetid: b6ac50b7-3ef1-43cf-8126-d9a003ebd825
ms.date: 12/05/2018
ms.keywords: CreatePresentationDescriptor, CreatePresentationDescriptor method [Media Foundation], CreatePresentationDescriptor method [Media Foundation],IMFMediaSource interface, IMFMediaSource interface [Media Foundation],CreatePresentationDescriptor method, IMFMediaSource.CreatePresentationDescriptor, IMFMediaSource::CreatePresentationDescriptor, b6ac50b7-3ef1-43cf-8126-d9a003ebd825, mf.imfmediasource_createpresentationdescriptor, mfidl/IMFMediaSource::CreatePresentationDescriptor
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaSource::CreatePresentationDescriptor
 - mfidl/IMFMediaSource::CreatePresentationDescriptor
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
 - IMFMediaSource.CreatePresentationDescriptor
---

# IMFMediaSource::CreatePresentationDescriptor


## -description

Retrieves a copy of the media source's presentation descriptor. Applications use the presentation descriptor to select streams and to get information about the source content.

## -parameters

### -param ppPresentationDescriptor [out]

Receives a pointer to the presentation descriptor's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor">IMFPresentationDescriptor</a> interface. The caller must release the interface.

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
The media source's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown">Shutdown</a> method has been called.

</td>
</tr>
</table>

## -remarks

The presentation descriptor contains the media source's default settings for the presentation. The application can change these settings by selecting or deselecting streams, or by changing the media type on a stream. Do not modify the presentation descriptor unless the source is stopped. The changes take affect when the source's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start">IMFMediaSource::Start</a> method is called.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a>



<a href="/windows/desktop/medfound/media-sources">Media Sources</a>