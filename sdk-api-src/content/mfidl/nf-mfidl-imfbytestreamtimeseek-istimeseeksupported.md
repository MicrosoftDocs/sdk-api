---
UID: NF:mfidl.IMFByteStreamTimeSeek.IsTimeSeekSupported
title: IMFByteStreamTimeSeek::IsTimeSeekSupported
author: windows-sdk-content
description: Queries whether the byte stream supports time-based seeking.
old-location: mf\imfbytestreamtimeseek_istimeseeksupported.htm
tech.root: medfound
ms.assetid: 92FCE0EF-046C-4639-958E-731795C5A123
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IMFByteStreamTimeSeek interface [Media Foundation],IsTimeSeekSupported method, IMFByteStreamTimeSeek.IsTimeSeekSupported, IMFByteStreamTimeSeek::IsTimeSeekSupported, IsTimeSeekSupported, IsTimeSeekSupported method [Media Foundation], IsTimeSeekSupported method [Media Foundation],IMFByteStreamTimeSeek interface, mf.imfbytestreamtimeseek_istimeseeksupported, mfidl/IMFByteStreamTimeSeek::IsTimeSeekSupported
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
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
 - mfidl.h
api_name:
 - IMFByteStreamTimeSeek.IsTimeSeekSupported
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFByteStreamTimeSeek::IsTimeSeekSupported


## -description


Queries whether the byte stream supports time-based seeking.


## -parameters




### -param pfTimeSeekIsSupported [out]

Receives the value <b>TRUE</b> if the byte stream supports time-based seeking, or <b>FALSE</b> otherwise.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/BD9EDFF7-46BA-4788-A44E-C69C4B0BEB50">IMFByteStreamTimeSeek</a>
 

 

