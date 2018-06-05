---
UID: NF:thumbcache.IThumbnailSettings.SetContext
title: IThumbnailSettings::SetContext
author: windows-sdk-content
description: Enables a thumbnail provider to return a thumbnail specific to the user's context.
old-location: shell\IThumbnailSettings_SetContext.htm
old-project: shell
ms.assetid: AD333075-3358-4fee-BDEE-087B7012C93E
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IThumbnailSettings interface [Windows Shell],SetContext method, IThumbnailSettings.SetContext, IThumbnailSettings::SetContext, SetContext, SetContext method [Windows Shell], SetContext method [Windows Shell],IThumbnailSettings interface, shell.IThumbnailSettings_SetContext, thumbcache/IThumbnailSettings::SetContext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: thumbcache.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Thumbcache.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WTS_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Thumbcache.h
api_name:
-	IThumbnailSettings.SetContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

