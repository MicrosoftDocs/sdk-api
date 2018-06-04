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

# IXpsPrintJobStream::Close


## -description


<p class="CCE_Message">[IXpsPrintJobStream::Close is not supported and may be altered or unavailable in the future. ]

Closes the stream and indicates to the print job that the entire document has been written to the print queue by the application.


## -parameters






## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



After <b>Close</b> has been called, all subsequent attempts to write data to the stream will fail.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541159">Documents</a>



<a href="https://msdn.microsoft.com/a7855015-32db-48ff-8f8d-3d84d2843fde">IXpsPrintJobStream</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

