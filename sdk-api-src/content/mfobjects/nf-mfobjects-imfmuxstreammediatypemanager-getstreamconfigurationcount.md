---
UID: NF:mfobjects.IMFMuxStreamMediaTypeManager.GetStreamConfigurationCount
title: IMFMuxStreamMediaTypeManager::GetStreamConfigurationCount (mfobjects.h)
description: Gets the count of registered stream configurations, which define set of substreams that can be included the multiplexed output.
helpviewer_keywords: ["GetStreamConfigurationCount","GetStreamConfigurationCount method [Media Foundation]","GetStreamConfigurationCount method [Media Foundation]","IMFMuxStreamMediaTypeManager interface","IMFMuxStreamMediaTypeManager interface [Media Foundation]","GetStreamConfigurationCount method","IMFMuxStreamMediaTypeManager.GetStreamConfigurationCount","IMFMuxStreamMediaTypeManager::GetStreamConfigurationCount","mf.imfmuxstreammediatypemanager_getstreamconfigurationcount","mfobjects/IMFMuxStreamMediaTypeManager::GetStreamConfigurationCount"]
old-location: mf\imfmuxstreammediatypemanager_getstreamconfigurationcount.htm
tech.root: mf
ms.assetid: 9591BFEC-DD25-41A8-9DA8-7F39158CB442
ms.date: 12/05/2018
ms.keywords: GetStreamConfigurationCount, GetStreamConfigurationCount method [Media Foundation], GetStreamConfigurationCount method [Media Foundation],IMFMuxStreamMediaTypeManager interface, IMFMuxStreamMediaTypeManager interface [Media Foundation],GetStreamConfigurationCount method, IMFMuxStreamMediaTypeManager.GetStreamConfigurationCount, IMFMuxStreamMediaTypeManager::GetStreamConfigurationCount, mf.imfmuxstreammediatypemanager_getstreamconfigurationcount, mfobjects/IMFMuxStreamMediaTypeManager::GetStreamConfigurationCount
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
 - IMFMuxStreamMediaTypeManager::GetStreamConfigurationCount
 - mfobjects/IMFMuxStreamMediaTypeManager::GetStreamConfigurationCount
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
 - IMFMuxStreamMediaTypeManager.GetStreamConfigurationCount
---

# IMFMuxStreamMediaTypeManager::GetStreamConfigurationCount


## -description

Gets the count of registered stream configurations, which define set of substreams that can be included  the  multiplexed output.

## -parameters

### -param pdwCount [out]

The number of registered stream configurations.

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

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager">IMFMuxStreamMediaTypeManager</a>