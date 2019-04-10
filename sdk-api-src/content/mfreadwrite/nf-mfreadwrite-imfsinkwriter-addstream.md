---
UID: NF:mfreadwrite.IMFSinkWriter.AddStream
title: IMFSinkWriter::AddStream (mfreadwrite.h)
author: windows-sdk-content
description: Adds a stream to the sink writer.
old-location: mf\imfsinkwriter_addstream.htm
tech.root: medfound
ms.assetid: 9f9b1216-e915-4188-bcfd-6c41e1821ec4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddStream, AddStream method [Media Foundation], AddStream method [Media Foundation],IMFSinkWriter interface, IMFSinkWriter interface [Media Foundation],AddStream method, IMFSinkWriter.AddStream, IMFSinkWriter::AddStream, mf.imfsinkwriter_addstream, mfreadwrite/IMFSinkWriter::AddStream
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
 - IMFSinkWriter.AddStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSinkWriter::AddStream


## -description


Adds a stream to the sink writer.


## -parameters




### -param pTargetMediaType [in]

A pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of a media type. This media type specifies the format of the samples that will be written to the file. It does not need to match the input format. To set the input format, call <a href="https://msdn.microsoft.com/02a73f73-3b25-4578-9a7e-c9f8a4c8cd99">IMFSinkWriter::SetInputMediaType</a>.


### -param pdwStreamIndex [out]

Receives the zero-based index of the new stream.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a>



<a href="https://msdn.microsoft.com/23AF25B8-B94C-48BC-83D8-5863ACFFD4CA">Sink Writer</a>
 

 

