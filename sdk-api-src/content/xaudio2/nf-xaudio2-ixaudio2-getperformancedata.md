---
UID: NF:xaudio2.IXAudio2.GetPerformanceData
title: IXAudio2::GetPerformanceData (xaudio2.h)
description: Returns current resource usage details, such as available memory or CPU usage.
helpviewer_keywords: ["GetPerformanceData","GetPerformanceData method [XAudio2 Audio Mixing APIs]","GetPerformanceData method [XAudio2 Audio Mixing APIs]","IXAudio2 interface","IXAudio2 interface [XAudio2 Audio Mixing APIs]","GetPerformanceData method","IXAudio2.GetPerformanceData","IXAudio2::GetPerformanceData","xaudio2.ixaudio2_interface_getperformancedata","xaudio2/IXAudio2::GetPerformanceData"]
old-location: xaudio2\ixaudio2_interface_getperformancedata.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2.IXAudio2.GetPerformanceData(XAUDIO2_PERFORMANCE_DATA@)
ms.date: 12/05/2018
ms.keywords: GetPerformanceData, GetPerformanceData method [XAudio2 Audio Mixing APIs], GetPerformanceData method [XAudio2 Audio Mixing APIs],IXAudio2 interface, IXAudio2 interface [XAudio2 Audio Mixing APIs],GetPerformanceData method, IXAudio2.GetPerformanceData, IXAudio2::GetPerformanceData, xaudio2.ixaudio2_interface_getperformancedata, xaudio2/IXAudio2::GetPerformanceData
req.header: xaudio2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXAudio2::GetPerformanceData
 - xaudio2/IXAudio2::GetPerformanceData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.h
api_name:
 - IXAudio2.GetPerformanceData
---

# IXAudio2::GetPerformanceData


## -description

Returns current resource usage details, such as available memory or CPU usage.

## -parameters

### -param pPerfData [out]

On success, pointer to an <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_performance_data">XAUDIO2_PERFORMANCE_DATA</a> structure that is returned.

## -remarks

For specific information on the statistics returned by <b>GetPerformanceData</b>, see the <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_performance_data">XAUDIO2_PERFORMANCE_DATA</a> structure reference.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2">IXAudio2</a>