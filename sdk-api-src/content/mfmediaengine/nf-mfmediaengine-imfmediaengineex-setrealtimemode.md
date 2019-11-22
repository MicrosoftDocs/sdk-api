---
UID: NF:mfmediaengine.IMFMediaEngineEx.SetRealTimeMode
title: IMFMediaEngineEx::SetRealTimeMode (mfmediaengine.h)

description: Sets the real time mode used for the next call to SetSource or Load.
old-location: mf\imfmediaengineex_setrealtimemode.htm
tech.root: medfound
ms.assetid: 31534f69-33ec-41d3-93aa-f4c457649e48

ms.date: 12/05/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],SetRealTimeMode method, IMFMediaEngineEx.SetRealTimeMode, IMFMediaEngineEx::SetRealTimeMode, SetRealTimeMode, SetRealTimeMode method [Media Foundation], SetRealTimeMode method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_setrealtimemode, mfmediaengine/IMFMediaEngineEx::SetRealTimeMode
ms.topic: method
f1_keywords: 
 - "mfmediaengine/IMFMediaEngineEx.SetRealTimeMode"
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
 - IMFMediaEngineEx.SetRealTimeMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineEx::SetRealTimeMode


## -description


Sets the real time mode used for the next call to  <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsource">SetSource</a> or <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a>. 


## -parameters




### -param fEnable [in]

Specifies the real time mode.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>
 

 

