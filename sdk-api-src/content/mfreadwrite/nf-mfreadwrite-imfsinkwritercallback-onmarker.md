---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

