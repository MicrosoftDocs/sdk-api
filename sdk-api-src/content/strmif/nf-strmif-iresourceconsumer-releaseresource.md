---
UID: NF:strmif.IResourceConsumer.ReleaseResource
title: IResourceConsumer::ReleaseResource method
author: windows-driver-content
description: The ReleaseResource method requests the resource consumer to release the specified resource.
old-location: dshow\iresourceconsumer_releaseresource.htm
old-project: DirectShow
ms.assetid: 9f0a5830-dcaa-4020-9e78-0cbe64e13360
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IResourceConsumer, IResourceConsumer interface [DirectShow], ReleaseResource method, IResourceConsumer::ReleaseResource, IResourceConsumerReleaseResource, ReleaseResource method [DirectShow], ReleaseResource method [DirectShow], IResourceConsumer interface, ReleaseResource,IResourceConsumer.ReleaseResource, dshow.iresourceconsumer_releaseresource, strmif/IResourceConsumer::ReleaseResource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IResourceConsumer.ReleaseResource
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IResourceConsumer::ReleaseResource method


## -description



The <code>ReleaseResource</code> method requests the resource consumer to release the specified resource.




## -parameters




### -param idResource [in]

Resource identifier to be released.


## -returns



Returns S_OK if the consumer has released it and requires it again when it becomes available, or S_FALSE if the consumer has not released it but will use <a href="https://msdn.microsoft.com/a3779a8d-fe78-4f9b-af6c-7a25e0f07a86">IResourceManager::NotifyRelease</a> when it does.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/dda2b207-dcd8-42df-95a3-d4bfbb4a7fd8">IResourceConsumer Interface</a>
 

 

