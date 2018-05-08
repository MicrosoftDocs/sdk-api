---
UID: NF:mfidl.IMFByteStreamTimeSeek.TimeSeek
title: IMFByteStreamTimeSeek::TimeSeek
author: windows-driver-content
description: Seeks to a new position in the byte stream.
old-location: mf\imfbytestreamtimeseek_timeseek.htm
old-project: medfound
ms.assetid: 786F1299-A9E2-4B2C-A6AE-F88E6BF022DC
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: IMFByteStreamTimeSeek interface [Media Foundation],TimeSeek method, IMFByteStreamTimeSeek.TimeSeek, IMFByteStreamTimeSeek::TimeSeek, TimeSeek, TimeSeek method [Media Foundation], TimeSeek method [Media Foundation],IMFByteStreamTimeSeek interface, mf.imfbytestreamtimeseek_timeseek, mfidl/IMFByteStreamTimeSeek::TimeSeek
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfidl.h
api_name:
-	IMFByteStreamTimeSeek.TimeSeek
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFByteStreamTimeSeek::TimeSeek


## -description


Seeks to a new position in the byte stream.


## -parameters




### -param qwTimePosition

The new position, in 100-nanosecond units.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the byte stream reads from a server, it might cache the seek request until the next read request. Therefore, the byte stream might not send a request to the server immediately.




## -see-also




<a href="https://msdn.microsoft.com/BD9EDFF7-46BA-4788-A44E-C69C4B0BEB50">IMFByteStreamTimeSeek</a>
 

 

