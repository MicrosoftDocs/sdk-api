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

# IUPnPServiceDocumentAccess::GetDocumentURL


## -description


The <b>GetDocumentURL</b> method retrieves the Service Control Protocol Description (SCPD) URL for a service object. Using this URL, the UPnP control point can download the complete SCPD document.


## -parameters




### -param pbstrDocUrl [out]

The URL to the complete SCPD document.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns <b>E_FAIL</b>. This method will fail if called after a service enumeration has already started.




## -see-also




<a href="https://msdn.microsoft.com/A4890300-2945-4973-ACFC-F950C5E15A0E">IUPnPServiceDocumentAccess</a>



<a href="https://msdn.microsoft.com/B0C197A0-4987-43BD-A48D-BF2E6150A85F">IUPnPServiceDocumentAccess:GetDocument</a>
 

 

