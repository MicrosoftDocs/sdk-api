---
UID: NF:mfreadwrite.IMFSourceReaderCallback2.OnStreamError
title: IMFSourceReaderCallback2::OnStreamError
author: windows-sdk-content
description: Called when an asynchronous error occurs with the IMFSourceReader.
old-location: mf\imfsourcereadercallback2_onstreamerror.htm
old-project: medfound
ms.assetid: 9239DE9E-8CC3-493A-B7FE-AB0294907069
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IMFSourceReaderCallback2 interface [Media Foundation],OnStreamError method, IMFSourceReaderCallback2.OnStreamError, IMFSourceReaderCallback2::OnStreamError, OnStreamError, OnStreamError method [Media Foundation], OnStreamError method [Media Foundation],IMFSourceReaderCallback2 interface, mf.imfsourcereadercallback2_onstreamerror, mfreadwrite/IMFSourceReaderCallback2::OnStreamError
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfreadwrite.h
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
req.typenames: MF_SOURCE_READER_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfreadwrite.h
api_name:
 - IMFSourceReaderCallback2.OnStreamError
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSourceReaderCallback2::OnStreamError


## -description


Called when an asynchronous error occurs with the <a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a>.


## -parameters




### -param dwStreamIndex

The index of the stream of the transform that raised the asynchronous error.


### -param hrStatus

The error that occurred.


## -returns



Returns an <b>HRESULT</b> value. Currently, the source reader ignores the return value.




## -see-also




<a href="https://msdn.microsoft.com/D0EC7FE9-74C3-4A7C-A5F3-798A3D6EF2CC">IMFSourceReaderCallback2</a>
 

 

