---
UID: NF:wmsdkidl.IWMWriterSink.IsRealTime
title: IWMWriterSink::IsRealTime (wmsdkidl.h)
author: windows-sdk-content
description: The IsRealTime is called by the writer to determine whether the sink needs data units to be delivered in real time. It is up to you to decide whether your custom sink requires real-time delivery.
old-location: wmformat\iwmwritersink_isrealtime.htm
tech.root: wmformat
ms.assetid: 95a32114-4581-4870-8c7f-b79b5af8f0a4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMWriterSink interface [windows Media Format],IsRealTime method, IWMWriterSink.IsRealTime, IWMWriterSink::IsRealTime, IWMWriterSinkIsRealTime, IsRealTime, IsRealTime method [windows Media Format], IsRealTime method [windows Media Format],IWMWriterSink interface, wmformat.iwmwritersink_isrealtime, wmsdkidl/IWMWriterSink::IsRealTime
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMWriterSink.IsRealTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriterSink::IsRealTime


## -description



The <b>IsRealTime</b> is called by the writer to determine whether the sink needs data units to be delivered in real time. It is up to you to decide whether your custom sink requires real-time delivery.




## -parameters




### -param pfRealTime [out]

Pointer to a Boolean value that is True if the sink requires real time data unit delivery.


## -returns



This method is implemented by the application. It should always return S_OK.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757467(v=VS.85).aspx">IWMWriterSink Interface</a>
 

 

