---
UID: NF:mfreadwrite.IMFSourceReaderCallback.OnFlush
title: IMFSourceReaderCallback::OnFlush
author: windows-sdk-content
description: Called when the IMFSourceReader::Flush method completes.
old-location: mf\imfsourcereadercallback_onflush.htm
tech.root: medfound
ms.assetid: a8273b0a-a75a-453f-bb42-38d554e44262
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: IMFSourceReaderCallback interface [Media Foundation],OnFlush method, IMFSourceReaderCallback.OnFlush, IMFSourceReaderCallback::OnFlush, OnFlush, OnFlush method [Media Foundation], OnFlush method [Media Foundation],IMFSourceReaderCallback interface, mf.imfsourcereadercallback_onflush, mfreadwrite/IMFSourceReaderCallback::OnFlush
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - mfreadwrite.h
api_name:
 - IMFSourceReaderCallback.OnFlush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSourceReaderCallback::OnFlush


## -description


Called when the <a href="https://msdn.microsoft.com/34992c64-9956-4b23-a979-df7f678405b5">IMFSourceReader::Flush</a> method completes.


## -parameters




### -param dwStreamIndex

The index of the stream that was flushed, or <b>MF_SOURCE_READER_ALL_STREAMS</b> if all streams were flushed.


## -returns



Returns an <b>HRESULT</b> value. Currently, the source reader ignores the return value.




## -remarks



This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/fff8b6e6-5d56-4301-b3ce-f3ff49398593">IMFSourceReaderCallback</a>



<a href="https://msdn.microsoft.com/8a17a754-53ef-4c05-9189-7978d864b17a">Source Reader</a>
 

 

