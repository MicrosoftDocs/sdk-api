---
UID: NF:mfmediaengine.IMFMediaEngine.GetError
title: IMFMediaEngine::GetError (mfmediaengine.h)
description: Gets the most recent error status.
old-location: mf\imfmediaengine_geterror.htm
tech.root: medfound
ms.assetid: F8A51AF8-8D73-47BC-ADA2-7F5108587873
ms.date: 12/05/2018
ms.keywords: GetError, GetError method [Media Foundation], GetError method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetError method, IMFMediaEngine.GetError, IMFMediaEngine::GetError, mf.imfmediaengine_geterror, mfmediaengine/IMFMediaEngine::GetError
ms.topic: method
f1_keywords:
- mfmediaengine/IMFMediaEngine.GetError
dev_langs:
- c++
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
- IMFMediaEngine.GetError
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngine::GetError


## -description


Gets the most recent error status.


## -parameters




### -param ppError [out]

Receives either a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaerror">IMFMediaError</a> interface, or the value <b>NULL</b>. If the value is <b>non-NULL</b>, the caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method returns the last error status, if any, that resulted from loading the media source. If there has not been an error, <i>ppError</i> receives the value <b>NULL</b>.

This method corresponds to the <b>error</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>
 

 

