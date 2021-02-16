---
UID: NF:mfidl.IMFMediaStream.GetStreamDescriptor
title: IMFMediaStream::GetStreamDescriptor (mfidl.h)
description: Retrieves a stream descriptor for this media stream.
helpviewer_keywords: ["574eacfb-3acd-4b47-9c25-3a67aae01178","GetStreamDescriptor","GetStreamDescriptor method [Media Foundation]","GetStreamDescriptor method [Media Foundation]","IMFMediaStream interface","IMFMediaStream interface [Media Foundation]","GetStreamDescriptor method","IMFMediaStream.GetStreamDescriptor","IMFMediaStream::GetStreamDescriptor","mf.imfmediastream_getstreamdescriptor","mfidl/IMFMediaStream::GetStreamDescriptor"]
old-location: mf\imfmediastream_getstreamdescriptor.htm
tech.root: mf
ms.assetid: 574eacfb-3acd-4b47-9c25-3a67aae01178
ms.date: 12/05/2018
ms.keywords: 574eacfb-3acd-4b47-9c25-3a67aae01178, GetStreamDescriptor, GetStreamDescriptor method [Media Foundation], GetStreamDescriptor method [Media Foundation],IMFMediaStream interface, IMFMediaStream interface [Media Foundation],GetStreamDescriptor method, IMFMediaStream.GetStreamDescriptor, IMFMediaStream::GetStreamDescriptor, mf.imfmediastream_getstreamdescriptor, mfidl/IMFMediaStream::GetStreamDescriptor
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
 - IMFMediaStream::GetStreamDescriptor
 - mfidl/IMFMediaStream::GetStreamDescriptor
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
 - IMFMediaStream.GetStreamDescriptor
---

# IMFMediaStream::GetStreamDescriptor


## -description

Retrieves a stream descriptor for this media stream.

## -parameters

### -param ppStreamDescriptor [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor">IMFStreamDescriptor</a> interface. The caller must release the interface.

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

Do not modify the stream descriptor. To change the presentation, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor">IMFMediaSource::CreatePresentationDescriptor</a> and modify the presentation descriptor.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediastream">IMFMediaStream</a>



<a href="/windows/desktop/medfound/media-sources">Media Sources</a>