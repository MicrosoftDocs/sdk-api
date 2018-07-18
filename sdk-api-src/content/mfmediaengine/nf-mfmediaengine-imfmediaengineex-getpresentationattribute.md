---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetPresentationAttribute
title: IMFMediaEngineEx::GetPresentationAttribute
author: windows-sdk-content
description: Gets a presentation attribute from the media resource.
old-location: mf\imfmediaengineex_getpresentationattribute.htm
old-project: medfound
ms.assetid: 127667EA-8ED2-428E-8F6B-C280CF42E1C5
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetPresentationAttribute, GetPresentationAttribute method [Media Foundation], GetPresentationAttribute method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetPresentationAttribute method, IMFMediaEngineEx.GetPresentationAttribute, IMFMediaEngineEx::GetPresentationAttribute, mf.imfmediaengineex_getpresentationattribute, mfmediaengine/IMFMediaEngineEx::GetPresentationAttribute
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MF_MEDIA_ENGINE_KEYERR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineEx.GetPresentationAttribute
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngineEx::GetPresentationAttribute


## -description


Gets a presentation attribute from the media resource.


## -parameters




### -param guidMFAttribute [in]

The attribute to query.

For a list of presentation attributes, see <a href="https://msdn.microsoft.com/2a092a6a-956b-4c1f-955f-529ec08665fe">Presentation Descriptor Attributes</a>.


### -param pvValue [out]

A pointer to a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> that receives the value. The method fills the <b>PROPVARIANT</b> with a copy of the stored value. The caller must free the <b>PROPVARIANT</b> by calling <a href="https://msdn.microsoft.com/062b6065-a56f-4ecd-b232-3ba338a6d806">PropVariantClear</a>.




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>
 

 

