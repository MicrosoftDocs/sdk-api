---
UID: NF:xpsobjectmodel_2.IXpsOMPackageWriter3D.SetModelPrintTicket
title: IXpsOMPackageWriter3D::SetModelPrintTicket
author: windows-sdk-content
description: Creates a print ticket with the specified part.
old-location: xps\ixpsompackagewriter3d_setmodelprintticket.htm
old-project: printdocs
ms.assetid: 2CCA48A9-CB7C-40F9-8BE0-FEC74AA25902
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IXpsOMPackageWriter3D interface [XPS Documents and Packaging],SetModelPrintTicket method, IXpsOMPackageWriter3D.SetModelPrintTicket, IXpsOMPackageWriter3D::SetModelPrintTicket, SetModelPrintTicket, SetModelPrintTicket method [XPS Documents and Packaging], SetModelPrintTicket method [XPS Documents and Packaging],IXpsOMPackageWriter3D interface, xps.ixpsompackagewriter3d_setmodelprintticket, xpsobjectmodel_2/IXpsOMPackageWriter3D::SetModelPrintTicket
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel_2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XPS_DOCUMENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XpsObjectModel_2.h
api_name:
 - IXpsOMPackageWriter3D.SetModelPrintTicket
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
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
 

 

