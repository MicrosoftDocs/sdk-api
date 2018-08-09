---
UID: NF:wmdxva.IWMPlayerTimestampHook.MapTimestamp
title: IWMPlayerTimestampHook::MapTimestamp
author: windows-sdk-content
description: The MapTimestamp method is called by the WMV Decoder DMO to enable the source filter to provide the decoder with a time stamp. The decoder applies the time stamp to the sample before delivering the sample to the video renderer.
old-location: wmformat\iwmplayertimestamphook_maptimestamp.htm
old-project: wmformat
ms.assetid: 67da583f-85da-4a09-be2c-44cf96bf51e7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMPlayerTimestampHook interface [windows Media Format],MapTimestamp method, IWMPlayerTimestampHook.MapTimestamp, IWMPlayerTimestampHook::MapTimestamp, IWMPlayerTimestampHookMapTimestamp, MapTimestamp, MapTimestamp method [windows Media Format], MapTimestamp method [windows Media Format],IWMPlayerTimestampHook interface, wmdxva/IWMPlayerTimestampHook::MapTimestamp, wmformat.iwmplayertimestamphook_maptimestamp
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmdxva.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: ASF_INDEX_IDENTIFIER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmdxva.h
api_name:
 - IWMPlayerTimestampHook.MapTimestamp
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPlayerTimestampHook::MapTimestamp


## -description



The <b>MapTimestamp</b> method is called by the WMV Decoder DMO to enable the source filter to provide the decoder with a time stamp. The decoder applies the time stamp to the sample before delivering the sample to the video renderer.




## -parameters




### -param rtIn [in]

Time stamp previously applied by the DMO.


### -param prtOut [out]

Time stamp to be applied to the sample.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code .




## -see-also




<a href="https://msdn.microsoft.com/5cb2f564-88e3-4b60-bde3-6ccf69c97c48">Enabling DirectX Video Acceleration</a>



<a href="https://msdn.microsoft.com/8a1b3b1f-1c9c-429f-958e-757b383c7e2a">IWMPlayerTimestampHook Interface</a>
 

 

