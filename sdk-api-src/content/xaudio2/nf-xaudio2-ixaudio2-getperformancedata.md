---
UID: NF:xaudio2.IXAudio2.GetPerformanceData
title: IXAudio2::GetPerformanceData
author: windows-sdk-content
description: Returns current resource usage details, such as available memory or CPU usage.
old-location: xaudio2\ixaudio2_interface_getperformancedata.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2.IXAudio2.GetPerformanceData(XAUDIO2_PERFORMANCE_DATA@)
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetPerformanceData, GetPerformanceData method [XAudio2 Audio Mixing APIs], GetPerformanceData method [XAudio2 Audio Mixing APIs],IXAudio2 interface, IXAudio2 interface [XAudio2 Audio Mixing APIs],GetPerformanceData method, IXAudio2.GetPerformanceData, IXAudio2::GetPerformanceData, xaudio2.ixaudio2_interface_getperformancedata, xaudio2/IXAudio2::GetPerformanceData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: XAUDIO2_FILTER_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.h
api_name:
 - IXAudio2.GetPerformanceData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAudio2::GetPerformanceData


## -description


Returns current resource usage details, such as available memory or CPU usage.


## -parameters




### -param pPerfData [out]

On success, pointer to an <a href="https://msdn.microsoft.com/en-us/library/Ee419239(v=VS.85).aspx">XAUDIO2_PERFORMANCE_DATA</a> structure that is returned. 



## -returns



This method does not return a value.




## -remarks



For specific information on the statistics returned by <b>GetPerformanceData</b>, see the <a href="https://msdn.microsoft.com/en-us/library/Ee419239(v=VS.85).aspx">XAUDIO2_PERFORMANCE_DATA</a> structure reference.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee415908(v=VS.85).aspx">IXAudio2</a>
 

 

