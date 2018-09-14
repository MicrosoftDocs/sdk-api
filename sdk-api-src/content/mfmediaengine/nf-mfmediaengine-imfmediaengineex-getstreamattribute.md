---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetStreamAttribute
title: IMFMediaEngineEx::GetStreamAttribute
author: windows-sdk-content
description: Gets a stream-level attribute from the media resource.
old-location: mf\imfmediaengineex_getstreamattribute.htm
tech.root: medfound
ms.assetid: 2C64CD7B-F376-47DF-AD5A-DE5EBC665288
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: GetStreamAttribute, GetStreamAttribute method [Media Foundation], GetStreamAttribute method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetStreamAttribute method, IMFMediaEngineEx.GetStreamAttribute, IMFMediaEngineEx::GetStreamAttribute, mf.imfmediaengineex_getstreamattribute, mfmediaengine/IMFMediaEngineEx::GetStreamAttribute
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineEx.GetStreamAttribute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineEx::GetStreamAttribute


## -description


Gets a stream-level attribute from the media resource.


## -parameters




### -param dwStreamIndex [in]

The zero-based index of the stream. To get the number of streams, call <a href="https://msdn.microsoft.com/7F3E805A-FE5C-4B75-9333-AE9819CFAFFA">IMFMediaEngineEx::GetNumberOfStreams</a>.


### -param guidMFAttribute [in]

The attribute to query. Possible values are listed in the following topics:


<ul>
<li>
<a href="https://msdn.microsoft.com/1364d7c5-67e8-49b6-8038-d6d4ea03fb7d">Stream Descriptor Attributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e84ba3f6-4857-4340-baca-5847650ea7b8">Media Type Attributes</a>
</li>
</ul>

### -param pvValue [out]

A pointer to a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> that receives the value. The method fills the <b>PROPVARIANT</b> with a copy of the stored value. Call <a href="https://msdn.microsoft.com/062b6065-a56f-4ecd-b232-3ba338a6d806">PropVariantClear</a> to free the memory allocated by the method.




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>
 

 

