---
UID: NF:mfobjects.IMFMuxStreamMediaTypeManager.RemoveStreamConfiguration
title: IMFMuxStreamMediaTypeManager::RemoveStreamConfiguration (mfobjects.h)
description: Unregisters a stream configuration, which defines a set of substreams that can be included the multiplexed output.
helpviewer_keywords: ["IMFMuxStreamMediaTypeManager interface [Media Foundation]","RemoveStreamConfiguration method","IMFMuxStreamMediaTypeManager.RemoveStreamConfiguration","IMFMuxStreamMediaTypeManager::RemoveStreamConfiguration","RemoveStreamConfiguration","RemoveStreamConfiguration method [Media Foundation]","RemoveStreamConfiguration method [Media Foundation]","IMFMuxStreamMediaTypeManager interface","mf.imfmuxstreammediatypemanager_removestreamconfiguration","mfobjects/IMFMuxStreamMediaTypeManager::RemoveStreamConfiguration"]
old-location: mf\imfmuxstreammediatypemanager_removestreamconfiguration.htm
tech.root: mf
ms.assetid: 8808DC0A-7675-4913-B4F1-B2FCCB3AFBBF
ms.date: 12/05/2018
ms.keywords: IMFMuxStreamMediaTypeManager interface [Media Foundation],RemoveStreamConfiguration method, IMFMuxStreamMediaTypeManager.RemoveStreamConfiguration, IMFMuxStreamMediaTypeManager::RemoveStreamConfiguration, RemoveStreamConfiguration, RemoveStreamConfiguration method [Media Foundation], RemoveStreamConfiguration method [Media Foundation],IMFMuxStreamMediaTypeManager interface, mf.imfmuxstreammediatypemanager_removestreamconfiguration, mfobjects/IMFMuxStreamMediaTypeManager::RemoveStreamConfiguration
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
 - IMFMuxStreamMediaTypeManager::RemoveStreamConfiguration
 - mfobjects/IMFMuxStreamMediaTypeManager::RemoveStreamConfiguration
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
 - IMFMuxStreamMediaTypeManager.RemoveStreamConfiguration
---

# IMFMuxStreamMediaTypeManager::RemoveStreamConfiguration


## -description

Unregisters a stream configuration, which defines a set of substreams that can be included  the  multiplexed output.

## -parameters

### -param ullStreamMask [in]

A bitmask value where the bits that are on represent the indices of the substreams that are included in the stream configuration.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified configuration is not currently registered.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to complete the operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager">IMFMuxStreamMediaTypeManager</a>