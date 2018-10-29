---
UID: NF:mfreadwrite.IMFSinkWriterCallback2.OnStreamError
title: IMFSinkWriterCallback2::OnStreamError
author: windows-sdk-content
description: Called when an asynchronous error occurs with the IMFSinkWriter.
old-location: mf\imfsinkwritercallback2_onstreamerror.htm
tech.root: medfound
ms.assetid: 31239998-9D12-46A4-B3F3-68167F6EFFDD
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMFSinkWriterCallback2 interface [Media Foundation],OnStreamError method, IMFSinkWriterCallback2.OnStreamError, IMFSinkWriterCallback2::OnStreamError, OnStreamError, OnStreamError method [Media Foundation], OnStreamError method [Media Foundation],IMFSinkWriterCallback2 interface, mf.imfsinkwritercallback2_onstreamerror, mfreadwrite/IMFSinkWriterCallback2::OnStreamError
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMFSinkWriterCallback2.OnStreamError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSinkWriterCallback2::OnStreamError


## -description


Called when an asynchronous error occurs with the <a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a>.


## -parameters




### -param dwStreamIndex

The index of the stream of the transform that raised the asynchronous error.


### -param hrStatus

The error that occurred.


## -returns



Returns an <b>HRESULT</b> value. Currently, the sink writer ignores the return value.




## -see-also




<a href="https://msdn.microsoft.com/92885A3C-137D-42DD-A65D-D2CE56A69A68">IMFSinkWriterCallback2</a>
 

 

