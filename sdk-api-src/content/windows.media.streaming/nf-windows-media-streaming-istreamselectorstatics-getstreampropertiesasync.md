---
UID: NF:windows.media.streaming.IStreamSelectorStatics.GetStreamPropertiesAsync
title: IStreamSelectorStatics::streaming (windows.media.streaming.h)
description: When implemented gets the properties of the stream asynchronously.
helpviewer_keywords: ["GetStreamPropertiesAsync","GetStreamPropertiesAsync method [Media Streaming API]","GetStreamPropertiesAsync method [Media Streaming API]","IStreamSelectorStatics interface","IStreamSelectorStatics interface [Media Streaming API]","GetStreamPropertiesAsync method","IStreamSelectorStatics.GetStreamPropertiesAsync","IStreamSelectorStatics.streaming","IStreamSelectorStatics::GetStreamPropertiesAsync","IStreamSelectorStatics::streaming","mediastreaming.istreamselectorstatics_getstreampropertiesasync","windows/IStreamSelectorStatics::GetStreamPropertiesAsync"]
old-location: mediastreaming\istreamselectorstatics_getstreampropertiesasync.htm
tech.root: mediastreaming
ms.assetid: 8C1B6DC6-D85E-406F-B6DA-914DC5269666
ms.date: 12/05/2018
ms.keywords: GetStreamPropertiesAsync, GetStreamPropertiesAsync method [Media Streaming API], GetStreamPropertiesAsync method [Media Streaming API],IStreamSelectorStatics interface, IStreamSelectorStatics interface [Media Streaming API],GetStreamPropertiesAsync method, IStreamSelectorStatics.GetStreamPropertiesAsync, IStreamSelectorStatics.streaming, IStreamSelectorStatics::GetStreamPropertiesAsync, IStreamSelectorStatics::streaming, mediastreaming.istreamselectorstatics_getstreampropertiesasync, windows/IStreamSelectorStatics::GetStreamPropertiesAsync
req.header: windows.media.streaming.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStreamSelectorStatics::GetStreamPropertiesAsync
 - windows.media.streaming/IStreamSelectorStatics::GetStreamPropertiesAsync
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.media.streaming.h
api_name:
 - IStreamSelectorStatics.GetStreamPropertiesAsync
---

# IStreamSelectorStatics::streaming


## -description

When implemented gets the properties of the stream asynchronously.

## -parameters

### -param storageFile [in]

Windows.Storage.StorageFile

### -param selectorProperties [in]

An IPropertySet containing any of the following allowed values.

<ul>
<li><b>STREAM_SELECTOR_PROPERTY_BEST_URL_ONLY</b></li>
<li><b>STREAM_SELECTOR_PROPERTY_HTTP_ONLY</b></li>
<li><b>STREAM_SELECTOR_PROPERTY_LINK_BANDWIDTH</b></li>
<li><b>STREAM_SELECTOR_PROPERTY_PREFER_NO_TRANSCODING</b></li>
<li><b>STREAM_SELECTOR_PROPERTY_MAX_HEIGHT</b></li>
<li><b>STREAM_SELECTOR_PROPERTY_MAX_WIDTH</b></li>
</ul>

### -param value [out, retval]

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
</table>

## -see-also

<a href="/previous-versions/windows/desktop/legacy/hh828953(v=vs.85)">IStreamSelectorStatics</a>