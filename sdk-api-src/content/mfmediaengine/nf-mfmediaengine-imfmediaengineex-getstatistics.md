---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetStatistics
title: IMFMediaEngineEx::GetStatistics (mfmediaengine.h)

description: Gets a playback statistic from the Media Engine.
old-location: mf\imfmediaengineex_getstatistics.htm
tech.root: medfound
ms.assetid: 3C2FDE86-2EBD-4A5C-BD02-90613DBFDE65

ms.date: 12/05/2018
ms.keywords: GetStatistics, GetStatistics method [Media Foundation], GetStatistics method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetStatistics method, IMFMediaEngineEx.GetStatistics, IMFMediaEngineEx::GetStatistics, mf.imfmediaengineex_getstatistics, mfmediaengine/IMFMediaEngineEx::GetStatistics
ms.topic: method
f1_keywords: 
 - "mfmediaengine/IMFMediaEngineEx.GetStatistics"
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
 - IMFMediaEngineEx.GetStatistics
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineEx::GetStatistics


## -description


Gets a playback statistic from the Media Engine.


## -parameters




### -param StatisticID [in]

A member of the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_statistic">MF_MEDIA_ENGINE_STATISTIC</a> enumeration that identifies the statistic to get.


### -param pStatistic [out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> that receives the statistic. The data type and meaning of this value depends on the value of <i>StatisticID</i>. The caller must free the <b>PROPVARIANT</b> by calling <a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-propvariantclear">PropVariantClear</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>
 

 

