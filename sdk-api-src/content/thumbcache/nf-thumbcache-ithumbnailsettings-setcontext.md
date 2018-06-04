---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IThumbnailSettings::SetContext


## -description


Enables a thumbnail provider to return a thumbnail specific to the user's context.

Initially, a thumbnail provider receives a request for a thumbnail image through a call to the <a href="https://msdn.microsoft.com/0fcfe68b-5d36-4be1-a468-b5c2d7af0651">IThumbnailCache::GetThumbnail</a> method. In response, before the provider calls <a href="https://msdn.microsoft.com/7c40e2cf-c706-4a4a-819f-a416d6846158">IExtractImage::Extract</a> or <a href="https://msdn.microsoft.com/5ea237fb-6b1c-4e87-a9f3-711ffa37b3dc">IThumbnailProvider::GetThumbnail</a>, the thumbnail cache can call <b>IThumbnailSettings::SetContext</b> to ensure that the thumbnail that is returned is appropriate to the user's context. For example, the provider could detect the new <b>WTS_APPSTYLE</b> flag and return a thumbnail that conforms to the Windows 8 UI guidelines.


## -parameters




### -param dwContext [in]

Type: <b><a href="https://msdn.microsoft.com/062B148E-19FB-4bcd-82CE-669B2ACD0BF6">WTS_CONTEXTFLAGS</a></b>

One or more flags that specify the context. This value is based on the <a href="https://msdn.microsoft.com/D9C84E86-35AF-437f-966E-BABD02B824C0">WTS_FLAGS</a> values that are received by the thumbnail provider through the call to <a href="https://msdn.microsoft.com/5ea237fb-6b1c-4e87-a9f3-711ffa37b3dc">IThumbnailProvider::GetThumbnail</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/502537E5-1D72-44f0-BC75-DBED61F174FC">IThumbnailSettings</a>
 

 

