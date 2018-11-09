---
UID: NF:mfobjects.IMFMuxStreamAttributesManager.GetStreamCount
title: IMFMuxStreamAttributesManager::GetStreamCount
author: windows-sdk-content
description: Gets the count of substreams managed by the multiplexed media source.
old-location: mf\imfmuxstreamattributesmanager_getstreamcount.htm
tech.root: medfound
ms.assetid: 631802B5-00F7-4219-9B21-5A1FB8628477
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetStreamCount, GetStreamCount method [Media Foundation], GetStreamCount method [Media Foundation],IMFMuxStreamAttributesManager interface, IMFMuxStreamAttributesManager interface [Media Foundation],GetStreamCount method, IMFMuxStreamAttributesManager.GetStreamCount, IMFMuxStreamAttributesManager::GetStreamCount, mf.imfmuxstreamattributesmanager_getstreamcount, mfobjects/IMFMuxStreamAttributesManager::GetStreamCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMFMuxStreamAttributesManager.GetStreamCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMuxStreamAttributesManager::GetStreamCount


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




<a href="https://msdn.microsoft.com/BBDAEF1C-DFEC-4647-8B74-E2ABB25F87CC">IMFMuxStreamMediaTypeManager</a>
 

 

