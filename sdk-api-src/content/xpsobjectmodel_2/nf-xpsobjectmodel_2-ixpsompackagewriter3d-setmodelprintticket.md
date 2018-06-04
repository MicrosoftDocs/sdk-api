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

# IXpsOMPackageWriter3D::SetModelPrintTicket


## -description


Creates a print ticket with the specified part.


## -parameters




### -param printTicketPartName [in]

The part is added to package and becomes a target of relationship from model part. 


### -param printTicketData [in]

A readable stream that  holds the 3D model print ticket.


## -returns



Returns the appropriate HRESULT error code. Calling this method more than once per package writer returns the error XPS_E_MULTIPLE_PRINTICKETS_ON_DOCUMENT. 




## -remarks



Call this method at most once per package writer. Calling this method creates a part with content type “application/vnd.ms-printing.printticket+xml”. It is linked from model part with relationship type “http://schemas.microsoft.com/3dmanufacturing/2013/01/printticket” .




## -see-also




<a href="https://msdn.microsoft.com/2F3E0529-7E2B-4BCD-AE8F-D0F3259D1A48">IXpsOMPackageWriter3D</a>
 

 

