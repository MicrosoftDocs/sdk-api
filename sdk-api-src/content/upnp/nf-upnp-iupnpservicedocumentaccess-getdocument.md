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

# IUPnPServiceDocumentAccess::GetDocument


## -description


The <b>GetDocument</b> method retrieves the Service Control Protocol Description (SCPD) document for a service object. The information provided by this document enables the user to pre-determine which actions are supported by the service, or review information about state variables.


## -parameters




### -param pbstrDoc [out]

The  complete SCPD document.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns <b>E_FAIL</b>.




## -see-also




<a href="https://msdn.microsoft.com/A4890300-2945-4973-ACFC-F950C5E15A0E">IUPnPServiceDocumentAccess</a>



<a href="https://msdn.microsoft.com/57AF4510-89D6-4DD5-B164-1478A5C27E20">IUPnPServiceDocumentAccess::GetDocumentURL</a>
 

 

