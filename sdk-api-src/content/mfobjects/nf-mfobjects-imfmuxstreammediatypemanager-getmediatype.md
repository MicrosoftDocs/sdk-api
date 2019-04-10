---
UID: NF:mfobjects.IMFMuxStreamMediaTypeManager.GetMediaType
title: IMFMuxStreamMediaTypeManager::GetMediaType (mfobjects.h)
author: windows-sdk-content
description: Gets the IMFMediaType of the substream with the specified index.
old-location: mf\imfmuxstreammediatypemanager_getmediatype.htm
tech.root: medfound
ms.assetid: F8A65783-7FD8-46C2-87B0-BC540E1F187F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetMediaType, GetMediaType method [Media Foundation], GetMediaType method [Media Foundation],IMFMuxStreamMediaTypeManager interface, IMFMuxStreamMediaTypeManager interface [Media Foundation],GetMediaType method, IMFMuxStreamMediaTypeManager.GetMediaType, IMFMuxStreamMediaTypeManager::GetMediaType, mf.imfmuxstreammediatypemanager_getmediatype, mfobjects/IMFMuxStreamMediaTypeManager::GetMediaType
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
 - IMFMuxStreamMediaTypeManager.GetMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMuxStreamMediaTypeManager::GetMediaType


## -description


Gets the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> of the substream with the specified index.


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
The stream specified substream index is invalid. Call <a href="https://msdn.microsoft.com/631802B5-00F7-4219-9B21-5A1FB8628477">GetStreamCount</a> to get the number of substreams managed by the multiplexed media source.

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




<a href="https://msdn.microsoft.com/BBDAEF1C-DFEC-4647-8B74-E2ABB25F87CC">IMFMuxStreamMediaTypeManager</a>
 

 

