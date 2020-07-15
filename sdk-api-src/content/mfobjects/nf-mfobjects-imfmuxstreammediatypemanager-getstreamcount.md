---
UID: NF:mfobjects.IMFMuxStreamMediaTypeManager.GetStreamCount
title: IMFMuxStreamMediaTypeManager::GetStreamCount (mfobjects.h)
description: Gets the count of substreams managed by the multiplexed media source.
helpviewer_keywords: ["GetStreamCount","GetStreamCount method [Media Foundation]","GetStreamCount method [Media Foundation]","IMFMuxStreamMediaTypeManager interface","IMFMuxStreamMediaTypeManager interface [Media Foundation]","GetStreamCount method","IMFMuxStreamMediaTypeManager.GetStreamCount","IMFMuxStreamMediaTypeManager::GetStreamCount","mf.imfmuxstreammediatypemanager_getstreamcount","mfobjects/IMFMuxStreamMediaTypeManager::GetStreamCount"]
old-location: mf\imfmuxstreammediatypemanager_getstreamcount.htm
tech.root: medfound
ms.assetid: EEEF5D71-22C4-4050-9088-8BAC554EB66E
ms.date: 12/05/2018
ms.keywords: GetStreamCount, GetStreamCount method [Media Foundation], GetStreamCount method [Media Foundation],IMFMuxStreamMediaTypeManager interface, IMFMuxStreamMediaTypeManager interface [Media Foundation],GetStreamCount method, IMFMuxStreamMediaTypeManager.GetStreamCount, IMFMuxStreamMediaTypeManager::GetStreamCount, mf.imfmuxstreammediatypemanager_getstreamcount, mfobjects/IMFMuxStreamMediaTypeManager::GetStreamCount
f1_keywords:
- mfobjects/IMFMuxStreamMediaTypeManager.GetStreamCount
dev_langs:
- c++
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
- IMFMuxStreamMediaTypeManager.GetStreamCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMuxStreamMediaTypeManager::GetStreamCount


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




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager">IMFMuxStreamMediaTypeManager</a>
 

 

