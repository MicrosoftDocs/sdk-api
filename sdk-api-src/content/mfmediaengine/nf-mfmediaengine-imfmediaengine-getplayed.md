---
UID: NF:mfmediaengine.IMFMediaEngine.GetPlayed
title: IMFMediaEngine::GetPlayed
author: windows-sdk-content
description: Gets the time ranges that have been rendered.
old-location: mf\imfmediaengine_getplayed.htm
old-project: medfound
ms.assetid: E74D1785-E8BA-4B3A-9FF8-63FBDED5FA9E
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetPlayed, GetPlayed method [Media Foundation], GetPlayed method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetPlayed method, IMFMediaEngine.GetPlayed, IMFMediaEngine::GetPlayed, mf.imfmediaengine_getplayed, mfmediaengine/IMFMediaEngine::GetPlayed
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
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFMediaEngine.GetPlayed
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngine::GetPlayed


## -description


Gets the time ranges that have been rendered.


## -parameters




### -param ppPlayed [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/E39646E6-66F4-4413-A84B-43039689AEE7">IMFMediaTimeRange</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method corresponds to the <b>played</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>
 

 

