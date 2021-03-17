---
UID: NF:mfobjects.IMFMuxStreamAttributesManager.GetAttributes
title: IMFMuxStreamAttributesManager::GetAttributes (mfobjects.h)
description: Gets the IMFAttributes for the substream with the specified index.
helpviewer_keywords: ["GetAttributes","GetAttributes method [Media Foundation]","GetAttributes method [Media Foundation]","IMFMuxStreamAttributesManager interface","IMFMuxStreamAttributesManager interface [Media Foundation]","GetAttributes method","IMFMuxStreamAttributesManager.GetAttributes","IMFMuxStreamAttributesManager::GetAttributes","mf.imfmuxstreamattributesmanager_getattributes","mfobjects/IMFMuxStreamAttributesManager::GetAttributes"]
old-location: mf\imfmuxstreamattributesmanager_getattributes.htm
tech.root: mf
ms.assetid: 1C00900F-BD8B-4AF7-82E0-37AC370A90E3
ms.date: 12/05/2018
ms.keywords: GetAttributes, GetAttributes method [Media Foundation], GetAttributes method [Media Foundation],IMFMuxStreamAttributesManager interface, IMFMuxStreamAttributesManager interface [Media Foundation],GetAttributes method, IMFMuxStreamAttributesManager.GetAttributes, IMFMuxStreamAttributesManager::GetAttributes, mf.imfmuxstreamattributesmanager_getattributes, mfobjects/IMFMuxStreamAttributesManager::GetAttributes
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
 - IMFMuxStreamAttributesManager::GetAttributes
 - mfobjects/IMFMuxStreamAttributesManager::GetAttributes
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
 - IMFMuxStreamAttributesManager.GetAttributes
---

# IMFMuxStreamAttributesManager::GetAttributes


## -description

Gets the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> for the substream with the specified index.

## -parameters

### -param dwMuxStreamIndex [in]

The index of the substream for which attributes are retrieved.

### -param ppStreamAttributes [in]

The attributes for the specified substream.

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
</table>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager">IMFMuxStreamMediaTypeManager</a>