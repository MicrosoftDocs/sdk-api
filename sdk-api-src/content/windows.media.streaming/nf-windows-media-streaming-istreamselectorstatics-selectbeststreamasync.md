---
UID: NF:windows.media.streaming.IStreamSelectorStatics.SelectBestStreamAsync
title: IStreamSelectorStatics::streaming (windows.media.streaming.h)
description: When implemented queries asynchronously for the best stream.
helpviewer_keywords: ["IStreamSelectorStatics interface [Media Streaming API]","SelectBestStreamAsync method","IStreamSelectorStatics.SelectBestStreamAsync","IStreamSelectorStatics.streaming","IStreamSelectorStatics::SelectBestStreamAsync","IStreamSelectorStatics::streaming","SelectBestStreamAsync","SelectBestStreamAsync method [Media Streaming API]","SelectBestStreamAsync method [Media Streaming API]","IStreamSelectorStatics interface","mediastreaming.istreamselectorstatics_selectbeststreamasync","windows/IStreamSelectorStatics::SelectBestStreamAsync"]
old-location: mediastreaming\istreamselectorstatics_selectbeststreamasync.htm
tech.root: mediastreaming
ms.assetid: 7DE96557-2CA0-4A88-AFF1-6A5480EEE04D
ms.date: 12/05/2018
ms.keywords: IStreamSelectorStatics interface [Media Streaming API],SelectBestStreamAsync method, IStreamSelectorStatics.SelectBestStreamAsync, IStreamSelectorStatics.streaming, IStreamSelectorStatics::SelectBestStreamAsync, IStreamSelectorStatics::streaming, SelectBestStreamAsync, SelectBestStreamAsync method [Media Streaming API], SelectBestStreamAsync method [Media Streaming API],IStreamSelectorStatics interface, mediastreaming.istreamselectorstatics_selectbeststreamasync, windows/IStreamSelectorStatics::SelectBestStreamAsync
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
 - IStreamSelectorStatics::SelectBestStreamAsync
 - windows.media.streaming/IStreamSelectorStatics::SelectBestStreamAsync
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
 - IStreamSelectorStatics.SelectBestStreamAsync
---

# IStreamSelectorStatics::streaming


## -description

When implemented queries asynchronously for the best stream.

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