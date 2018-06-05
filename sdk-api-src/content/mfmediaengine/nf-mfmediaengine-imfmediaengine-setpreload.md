---
UID: NF:mfmediaengine.IMFMediaEngine.SetPreload
title: IMFMediaEngine::SetPreload
author: windows-sdk-content
description: Sets the preload flag.
old-location: mf\imfmediaengine_setpreload.htm
old-project: medfound
ms.assetid: 3480C16F-E4E4-469C-BE27-711044691A49
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],SetPreload method, IMFMediaEngine.SetPreload, IMFMediaEngine::SetPreload, SetPreload, SetPreload method [Media Foundation], SetPreload method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_setpreload, mfmediaengine/IMFMediaEngine::SetPreload
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFMediaEngine.SetPreload
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngine::SetPreload


## -description


Sets the preload flag.


## -parameters




### -param Preload [in]

An <a href="https://msdn.microsoft.com/784B3B3F-0A9E-4E34-9197-CE20E2F3FF78">MF_MEDIA_ENGINE_PRELOAD</a> value equal to  the preload flag.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method corresponds to setting the <b>preload</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5. The value is a hint to the user-agent whether to preload the media resource.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>
 

 

