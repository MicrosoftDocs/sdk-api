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

# IUPnPHttpHeaderControl::AddRequestHeaders


## -description


The <a href="https://msdn.microsoft.com/aed33117-9bfd-4a23-998f-4b8d040d6e3b">IUPnPHttpHeaderControl</a>::<b>AddRequestHeaders</b> method adds the supplied HTTP header to an HTTP request.


## -parameters




### -param bstrHttpHeaders [in]

String value that contains the HTTP header to attach to the request. For example, "User-Agent: DLNADOC/1.50\r\n".


<div class="alert"><b>Note</b>  For Windows 7 and Windows Server 2008 R2, only the User Agent HTTP header is supported.</div>
<div> </div>



## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/aed33117-9bfd-4a23-998f-4b8d040d6e3b">IUPnPHttpHeaderControl</a>
 

 

