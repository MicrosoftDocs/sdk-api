---
UID: NF:mfobjects.IMFMuxStreamMediaTypeManager.GetStreamConfiguration
title: IMFMuxStreamMediaTypeManager::GetStreamConfiguration (mfobjects.h)
description: Gets the stream configuration with the specified index, which defines a set of substreams that can be included the multiplexed output.
helpviewer_keywords: ["GetStreamConfiguration","GetStreamConfiguration method [Media Foundation]","GetStreamConfiguration method [Media Foundation]","IMFMuxStreamMediaTypeManager interface","IMFMuxStreamMediaTypeManager interface [Media Foundation]","GetStreamConfiguration method","IMFMuxStreamMediaTypeManager.GetStreamConfiguration","IMFMuxStreamMediaTypeManager::GetStreamConfiguration","mf.imfmuxstreammediatypemanager_getstreamconfiguration","mfobjects/IMFMuxStreamMediaTypeManager::GetStreamConfiguration"]
old-location: mf\imfmuxstreammediatypemanager_getstreamconfiguration.htm
tech.root: mf
ms.assetid: 5B2B7F8C-0D3B-4BBB-8445-1A428A29A272
ms.date: 12/05/2018
ms.keywords: GetStreamConfiguration, GetStreamConfiguration method [Media Foundation], GetStreamConfiguration method [Media Foundation],IMFMuxStreamMediaTypeManager interface, IMFMuxStreamMediaTypeManager interface [Media Foundation],GetStreamConfiguration method, IMFMuxStreamMediaTypeManager.GetStreamConfiguration, IMFMuxStreamMediaTypeManager::GetStreamConfiguration, mf.imfmuxstreammediatypemanager_getstreamconfiguration, mfobjects/IMFMuxStreamMediaTypeManager::GetStreamConfiguration
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
 - IMFMuxStreamMediaTypeManager::GetStreamConfiguration
 - mfobjects/IMFMuxStreamMediaTypeManager::GetStreamConfiguration
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
 - IMFMuxStreamMediaTypeManager.GetStreamConfiguration
---

# IMFMuxStreamMediaTypeManager::GetStreamConfiguration


## -description

Gets the stream configuration with the specified index, which defines a set of substreams that can be included  the  multiplexed output.

## -parameters

### -param ulIndex [in]

The index of the configuration to retrieve.

### -param pullStreamMask [out]

The index of the configuration to retrieve.

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
<dt><b>MF_E_INVALIDINDEX</b></dt>
</dl>
</td>
<td width="60%">
The specified configuration index is not valid.

</td>
</tr>
</table>

## -remarks

Stream configurations are ordered within the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager">IMFMuxStreamMediaTypeManager</a> by the numeric value of the bitmask.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager">IMFMuxStreamMediaTypeManager</a>