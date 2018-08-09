---
UID: NF:mfmediaengine.IMFMediaEngineProtectedContent.GetRequiredProtections
title: IMFMediaEngineProtectedContent::GetRequiredProtections
author: windows-sdk-content
description: Gets the content protections that must be applied in frame-server mode.
old-location: mf\imfmediaengineprotectedcontent_getrequiredprotections.htm
old-project: medfound
ms.assetid: 4D67813D-F222-4EB1-B059-6DB5EC642DA2
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetRequiredProtections, GetRequiredProtections method [Media Foundation], GetRequiredProtections method [Media Foundation],IMFMediaEngineProtectedContent interface, IMFMediaEngineProtectedContent interface [Media Foundation],GetRequiredProtections method, IMFMediaEngineProtectedContent.GetRequiredProtections, IMFMediaEngineProtectedContent::GetRequiredProtections, mf.imfmediaengineprotectedcontent_getrequiredprotections, mfmediaengine/IMFMediaEngineProtectedContent::GetRequiredProtections
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
 - IMFMediaEngineProtectedContent.GetRequiredProtections
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngineProtectedContent::GetRequiredProtections


## -description


Gets the content protections that must be applied in frame-server mode.


## -parameters




### -param pFrameProtectionFlags [out]

Receives a bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/6864ED4B-BB75-4176-992B-ABC95B81001A">MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS</a> enumeration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/85B37711-DB46-4BC7-A051-79E9507791FA">IMFMediaEngineProtectedContent</a>
 

 

