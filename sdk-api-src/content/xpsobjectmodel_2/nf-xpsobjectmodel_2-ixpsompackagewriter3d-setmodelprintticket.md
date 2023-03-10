---
UID: NF:xpsobjectmodel_2.IXpsOMPackageWriter3D.SetModelPrintTicket
title: IXpsOMPackageWriter3D::SetModelPrintTicket (xpsobjectmodel_2.h)
description: Creates a print ticket with the specified part.
helpviewer_keywords: ["IXpsOMPackageWriter3D interface [XPS Documents and Packaging]","SetModelPrintTicket method","IXpsOMPackageWriter3D.SetModelPrintTicket","IXpsOMPackageWriter3D::SetModelPrintTicket","SetModelPrintTicket","SetModelPrintTicket method [XPS Documents and Packaging]","SetModelPrintTicket method [XPS Documents and Packaging]","IXpsOMPackageWriter3D interface","xps.ixpsompackagewriter3d_setmodelprintticket","xpsobjectmodel_2/IXpsOMPackageWriter3D::SetModelPrintTicket"]
old-location: xps\ixpsompackagewriter3d_setmodelprintticket.htm
tech.root: xps
ms.assetid: 2CCA48A9-CB7C-40F9-8BE0-FEC74AA25902
ms.date: 12/05/2018
ms.keywords: IXpsOMPackageWriter3D interface [XPS Documents and Packaging],SetModelPrintTicket method, IXpsOMPackageWriter3D.SetModelPrintTicket, IXpsOMPackageWriter3D::SetModelPrintTicket, SetModelPrintTicket, SetModelPrintTicket method [XPS Documents and Packaging], SetModelPrintTicket method [XPS Documents and Packaging],IXpsOMPackageWriter3D interface, xps.ixpsompackagewriter3d_setmodelprintticket, xpsobjectmodel_2/IXpsOMPackageWriter3D::SetModelPrintTicket
req.header: xpsobjectmodel_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel_2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMPackageWriter3D::SetModelPrintTicket
 - xpsobjectmodel_2/IXpsOMPackageWriter3D::SetModelPrintTicket
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XpsObjectModel_2.h
api_name:
 - IXpsOMPackageWriter3D.SetModelPrintTicket
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

<a href="/windows/desktop/api/xpsobjectmodel_2/nn-xpsobjectmodel_2-ixpsompackagewriter3d">IXpsOMPackageWriter3D</a>