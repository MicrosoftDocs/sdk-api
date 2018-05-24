---
UID: NF:mfreadwrite.IMFSinkWriterCallback.OnMarker
title: IMFSinkWriterCallback::OnMarker
author: windows-driver-content
description: Called when the IMFSinkWriter::PlaceMarker method completes.
old-location: mf\imfsinkwritercallback_onmarker.htm
old-project: medfound
ms.assetid: 5b1ca6a7-c2bc-4b30-aa86-05bd4ccc052c
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IMFSinkWriterCallback interface [Media Foundation],OnMarker method, IMFSinkWriterCallback.OnMarker, IMFSinkWriterCallback::OnMarker, OnMarker, OnMarker method [Media Foundation], OnMarker method [Media Foundation],IMFSinkWriterCallback interface, mf.imfsinkwritercallback_onmarker, mfreadwrite/IMFSinkWriterCallback::OnMarker
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_SOURCE_READER_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfreadwrite.h
api_name:
-	IMFSinkWriterCallback.OnMarker
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSinkWriterCallback::OnMarker


## -description


Called when the <a href="https://msdn.microsoft.com/93140993-a926-437e-bc40-9b011c4c6832">IMFSinkWriter::PlaceMarker</a> method completes.


## -parameters




### -param dwStreamIndex [in]

The zero-based index of the stream. This parameter equals the value of the <i>dwStreamIndex</i> parameter in the <a href="https://msdn.microsoft.com/93140993-a926-437e-bc40-9b011c4c6832">PlaceMarker</a> method.


### -param pvContext [in]

The application-defined value that was given in the <i>pvContext</i> parameter in the <a href="https://msdn.microsoft.com/93140993-a926-437e-bc40-9b011c4c6832">PlaceMarker</a> method.


## -returns



Returns an <b>HRESULT</b> value. Currently, the sink writer ignores the return value.




## -remarks



This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/fa0295e6-473d-4304-9a7b-24584cade0a0">IMFSinkWriterCallback</a>



<a href="https://msdn.microsoft.com/23AF25B8-B94C-48BC-83D8-5863ACFFD4CA">Sink Writer</a>
 

 

