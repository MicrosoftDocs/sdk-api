---
UID: NF:mfobjects.IMFMuxStreamMediaTypeManager.GetMediaType
title: IMFMuxStreamMediaTypeManager::GetMediaType (mfobjects.h)
description: Gets the IMFMediaType of the substream with the specified index.
helpviewer_keywords: ["GetMediaType","GetMediaType method [Media Foundation]","GetMediaType method [Media Foundation]","IMFMuxStreamMediaTypeManager interface","IMFMuxStreamMediaTypeManager interface [Media Foundation]","GetMediaType method","IMFMuxStreamMediaTypeManager.GetMediaType","IMFMuxStreamMediaTypeManager::GetMediaType","mf.imfmuxstreammediatypemanager_getmediatype","mfobjects/IMFMuxStreamMediaTypeManager::GetMediaType"]
old-location: mf\imfmuxstreammediatypemanager_getmediatype.htm
tech.root: mf
ms.assetid: F8A65783-7FD8-46C2-87B0-BC540E1F187F
ms.date: 12/05/2018
ms.keywords: GetMediaType, GetMediaType method [Media Foundation], GetMediaType method [Media Foundation],IMFMuxStreamMediaTypeManager interface, IMFMuxStreamMediaTypeManager interface [Media Foundation],GetMediaType method, IMFMuxStreamMediaTypeManager.GetMediaType, IMFMuxStreamMediaTypeManager::GetMediaType, mf.imfmuxstreammediatypemanager_getmediatype, mfobjects/IMFMuxStreamMediaTypeManager::GetMediaType
req.header: mfobjects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMuxStreamMediaTypeManager::GetMediaType
 - mfobjects/IMFMuxStreamMediaTypeManager::GetMediaType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFMuxStreamMediaTypeManager.GetMediaType
---

# IMFMuxStreamMediaTypeManager::GetMediaType


## -description

Gets the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> of the substream with the specified index.

## -parameters

### -param dwMuxStreamIndex [in]

The index of the substream for which the media type is retrieved.

### -param ppMediaType [out]

The media type of the substream with the specified index.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
The stream specified substream index is invalid. Call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmuxstreamattributesmanager-getstreamcount">GetStreamCount</a> to get the number of substreams managed by the multiplexed media source.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDMEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
The media type of the specified substream is invalid. 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager">IMFMuxStreamMediaTypeManager</a>