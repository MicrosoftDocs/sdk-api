---
UID: NF:mfmediaengine.IMFMediaEngine.GetError
title: IMFMediaEngine::GetError
author: windows-sdk-content
description: Gets the most recent error status.
old-location: mf\imfmediaengine_geterror.htm
old-project: medfound
ms.assetid: F8A51AF8-8D73-47BC-ADA2-7F5108587873
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetError, GetError method [Media Foundation], GetError method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetError method, IMFMediaEngine.GetError, IMFMediaEngine::GetError, mf.imfmediaengine_geterror, mfmediaengine/IMFMediaEngine::GetError
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
 - IMFMediaEngine.GetError
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngine::GetError


## -description


Gets the most recent error status.


## -parameters




### -param ppError [out]

Receives either a pointer to the <a href="https://msdn.microsoft.com/08F161FE-C0E5-44EE-923E-646ADA534C42">IMFMediaError</a> interface, or the value <b>NULL</b>. If the value is <b>non-NULL</b>, the caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method returns the last error status, if any, that resulted from loading the media source. If there has not been an error, <i>ppError</i> receives the value <b>NULL</b>.

This method corresponds to the <b>error</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>
 

 

