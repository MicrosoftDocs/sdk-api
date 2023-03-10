---
UID: NF:mfobjects.IMFMuxStreamMediaTypeManager.AddStreamConfiguration
title: IMFMuxStreamMediaTypeManager::AddStreamConfiguration (mfobjects.h)
description: Registers a stream configuration, which defines a set of substreams that can be included the multiplexed output.
helpviewer_keywords: ["AddStreamConfiguration","AddStreamConfiguration method [Media Foundation]","AddStreamConfiguration method [Media Foundation]","IMFMuxStreamMediaTypeManager interface","IMFMuxStreamMediaTypeManager interface [Media Foundation]","AddStreamConfiguration method","IMFMuxStreamMediaTypeManager.AddStreamConfiguration","IMFMuxStreamMediaTypeManager::AddStreamConfiguration","mf.imfmuxstreammediatypemanager_addstreamconfiguration","mfobjects/IMFMuxStreamMediaTypeManager::AddStreamConfiguration"]
old-location: mf\imfmuxstreammediatypemanager_addstreamconfiguration.htm
tech.root: mf
ms.assetid: 9A647B60-ACA0-4878-A75B-54CA093DEDD0
ms.date: 12/05/2018
ms.keywords: AddStreamConfiguration, AddStreamConfiguration method [Media Foundation], AddStreamConfiguration method [Media Foundation],IMFMuxStreamMediaTypeManager interface, IMFMuxStreamMediaTypeManager interface [Media Foundation],AddStreamConfiguration method, IMFMuxStreamMediaTypeManager.AddStreamConfiguration, IMFMuxStreamMediaTypeManager::AddStreamConfiguration, mf.imfmuxstreammediatypemanager_addstreamconfiguration, mfobjects/IMFMuxStreamMediaTypeManager::AddStreamConfiguration
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
 - IMFMuxStreamMediaTypeManager::AddStreamConfiguration
 - mfobjects/IMFMuxStreamMediaTypeManager::AddStreamConfiguration
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
 - IMFMuxStreamMediaTypeManager.AddStreamConfiguration
---

# IMFMuxStreamMediaTypeManager::AddStreamConfiguration


## -description

Registers a stream configuration, which defines a set of substreams that can be included  the  multiplexed output.

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
The specified configuration is already registered.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The supplied bitmask has bits set that are invalid for the media source.

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

## -remarks

Stream configurations are ordered within the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager">IMFMuxStreamMediaTypeManager</a> by the numeric value of the bitmask.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager">IMFMuxStreamMediaTypeManager</a>