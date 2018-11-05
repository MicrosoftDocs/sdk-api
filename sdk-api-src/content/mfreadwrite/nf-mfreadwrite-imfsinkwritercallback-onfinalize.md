---
UID: NF:mfreadwrite.IMFSinkWriterCallback.OnFinalize
title: IMFSinkWriterCallback::OnFinalize
author: windows-sdk-content
description: Called when the IMFSinkWriter::Finalize method completes.
old-location: mf\imfsinkwritercallback_onfinalize.htm
tech.root: medfound
ms.assetid: 9da7bb55-bf9f-4579-ae8e-b33ce5461950
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IMFSinkWriterCallback interface [Media Foundation],OnFinalize method, IMFSinkWriterCallback.OnFinalize, IMFSinkWriterCallback::OnFinalize, OnFinalize, OnFinalize method [Media Foundation], OnFinalize method [Media Foundation],IMFSinkWriterCallback interface, mf.imfsinkwritercallback_onfinalize, mfreadwrite/IMFSinkWriterCallback::OnFinalize
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
 - IMFSinkWriterCallback.OnFinalize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSinkWriterCallback::OnFinalize


## -description


Called when the <a href="https://msdn.microsoft.com/352e6679-0710-429a-a659-47044ab60773">IMFSinkWriter::Finalize</a> method completes.


## -parameters




### -param hrStatus [in]

The status code for the <a href="https://msdn.microsoft.com/352e6679-0710-429a-a659-47044ab60773">Finalize</a> operation. If the value is an error code, the output file might be invalid.


## -returns



Returns an <b>HRESULT</b> value. Currently, the sink writer ignores the return value.




## -remarks



This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/fa0295e6-473d-4304-9a7b-24584cade0a0">IMFSinkWriterCallback</a>



<a href="https://msdn.microsoft.com/23AF25B8-B94C-48BC-83D8-5863ACFFD4CA">Sink Writer</a>
 

 

