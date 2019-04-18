---
UID: NF:mfobjects.IMFMuxStreamAttributesManager.GetAttributes
title: IMFMuxStreamAttributesManager::GetAttributes (mfobjects.h)
author: windows-sdk-content
description: Gets the IMFAttributes for the substream with the specified index.
old-location: mf\imfmuxstreamattributesmanager_getattributes.htm
tech.root: medfound
ms.assetid: 1C00900F-BD8B-4AF7-82E0-37AC370A90E3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAttributes, GetAttributes method [Media Foundation], GetAttributes method [Media Foundation],IMFMuxStreamAttributesManager interface, IMFMuxStreamAttributesManager interface [Media Foundation],GetAttributes method, IMFMuxStreamAttributesManager.GetAttributes, IMFMuxStreamAttributesManager::GetAttributes, mf.imfmuxstreamattributesmanager_getattributes, mfobjects/IMFMuxStreamAttributesManager::GetAttributes
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
 - IMFMuxStreamAttributesManager.GetAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMuxStreamAttributesManager::GetAttributes


## -description


Gets the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> for the substream with the specified index.


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
The stream specified substream index is invalid. Call <a href="https://msdn.microsoft.com/631802B5-00F7-4219-9B21-5A1FB8628477">GetStreamCount</a> to get the number of substreams managed by the multiplexed media source.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/BBDAEF1C-DFEC-4647-8B74-E2ABB25F87CC">IMFMuxStreamMediaTypeManager</a>
 

 

