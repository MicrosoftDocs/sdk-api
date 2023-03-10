---
UID: NF:mfobjects.IMFMuxStreamSampleManager.GetStreamCount
title: IMFMuxStreamSampleManager::GetStreamCount (mfobjects.h)
description: Gets the count of substreams managed by the multiplexed media source. (IMFMuxStreamSampleManager.GetStreamCount)
helpviewer_keywords: ["GetStreamCount","GetStreamCount method [Media Foundation]","GetStreamCount method [Media Foundation]","IMFMuxStreamSampleManager interface","IMFMuxStreamSampleManager interface [Media Foundation]","GetStreamCount method","IMFMuxStreamSampleManager.GetStreamCount","IMFMuxStreamSampleManager::GetStreamCount","mf.imfmuxstreamsamplemanager_getstreamcount","mfobjects/IMFMuxStreamSampleManager::GetStreamCount"]
old-location: mf\imfmuxstreamsamplemanager_getstreamcount.htm
tech.root: mf
ms.assetid: 7DB1AEAD-591F-4FA0-9DF0-9774C76A4B91
ms.date: 12/05/2018
ms.keywords: GetStreamCount, GetStreamCount method [Media Foundation], GetStreamCount method [Media Foundation],IMFMuxStreamSampleManager interface, IMFMuxStreamSampleManager interface [Media Foundation],GetStreamCount method, IMFMuxStreamSampleManager.GetStreamCount, IMFMuxStreamSampleManager::GetStreamCount, mf.imfmuxstreamsamplemanager_getstreamcount, mfobjects/IMFMuxStreamSampleManager::GetStreamCount
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
 - IMFMuxStreamSampleManager::GetStreamCount
 - mfobjects/IMFMuxStreamSampleManager::GetStreamCount
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
 - IMFMuxStreamSampleManager.GetStreamCount
---

# IMFMuxStreamSampleManager::GetStreamCount


## -description

Gets the count of substreams managed by the multiplexed media source.

## -parameters

### -param pdwMuxStreamCount [out]

The count of substreams managed by the multiplexed media source.

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
</table>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager">IMFMuxStreamSampleManager</a>
