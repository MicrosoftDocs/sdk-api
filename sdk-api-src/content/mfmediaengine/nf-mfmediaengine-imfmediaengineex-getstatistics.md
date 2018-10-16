---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetStatistics
title: IMFMediaEngineEx::GetStatistics
author: windows-sdk-content
description: Gets a playback statistic from the Media Engine.
old-location: mf\imfmediaengineex_getstatistics.htm
tech.root: medfound
ms.assetid: 3C2FDE86-2EBD-4A5C-BD02-90613DBFDE65
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: GetStatistics, GetStatistics method [Media Foundation], GetStatistics method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetStatistics method, IMFMediaEngineEx.GetStatistics, IMFMediaEngineEx::GetStatistics, mf.imfmediaengineex_getstatistics, mfmediaengine/IMFMediaEngineEx::GetStatistics
ms.prod: windows-hardware
ms.technology: windows-devices
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineEx::GetStatistics


## -description


Gets a playback statistic from the Media Engine.


## -parameters




### -param StatisticID [in]

A member of the <a href="https://msdn.microsoft.com/EB431C2F-69A3-4376-BEC7-A5AE0329AD15">MF_MEDIA_ENGINE_STATISTIC</a> enumeration that identifies the statistic to get.


### -param pStatistic [out]

A pointer to a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> that receives the statistic. The data type and meaning of this value depends on the value of <i>StatisticID</i>. The caller must free the <b>PROPVARIANT</b> by calling <a href="https://msdn.microsoft.com/062b6065-a56f-4ecd-b232-3ba338a6d806">PropVariantClear</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>
 

 

