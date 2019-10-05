---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetRealTimeMode
title: IMFMediaEngineEx::GetRealTimeMode (mfmediaengine.h)
author: windows-sdk-content
description: Gets the real time mode used for the next call to SetSource or Load.
old-location: mf\imfmediaengineex_getrealtimemode.htm
tech.root: medfound
ms.assetid: 473a2b5a-5b9d-4754-bd32-89c9c4ab8c4a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRealTimeMode, GetRealTimeMode method [Media Foundation], GetRealTimeMode method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetRealTimeMode method, IMFMediaEngineEx.GetRealTimeMode, IMFMediaEngineEx::GetRealTimeMode, mf.imfmediaengineex_getrealtimemode, mfmediaengine/IMFMediaEngineEx::GetRealTimeMode
ms.topic: method
f1_keywords: 
 - "mfmediaengine/IMFMediaEngineEx.GetRealTimeMode"
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
 - Mfmediaengine.h
api_name:
 - IMFMediaEngineEx.GetRealTimeMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineEx::GetRealTimeMode


## -description


Gets the real time mode used for the next call to <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsource">SetSource</a> or <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a>. 


## -parameters




### -param pfEnabled [out]

Receives the real time mode.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>
 

 

