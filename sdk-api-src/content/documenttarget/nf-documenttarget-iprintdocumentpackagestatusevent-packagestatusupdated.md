---
UID: NF:documenttarget.IPrintDocumentPackageStatusEvent.PackageStatusUpdated
title: IPrintDocumentPackageStatusEvent::PackageStatusUpdated (documenttarget.h)
description: Updates the status of the package when the print job in progress raises an event, or the job completes.
helpviewer_keywords: ["IPrintDocumentPackageStatusEvent interface [XPS Documents and Packaging]","PackageStatusUpdated method","IPrintDocumentPackageStatusEvent.PackageStatusUpdated","IPrintDocumentPackageStatusEvent::PackageStatusUpdated","PackageStatusUpdated","PackageStatusUpdated method [XPS Documents and Packaging]","PackageStatusUpdated method [XPS Documents and Packaging]","IPrintDocumentPackageStatusEvent interface","documenttarget/IPrintDocumentPackageStatusEvent::PackageStatusUpdated","xps.iprintdocumentpackagestatusevent_packagestatusupdated"]
old-location: xps\iprintdocumentpackagestatusevent_packagestatusupdated.htm
tech.root: xps
ms.assetid: A672E554-B117-475C-A01E-9FD4EA31621E
ms.date: 12/05/2018
ms.keywords: IPrintDocumentPackageStatusEvent interface [XPS Documents and Packaging],PackageStatusUpdated method, IPrintDocumentPackageStatusEvent.PackageStatusUpdated, IPrintDocumentPackageStatusEvent::PackageStatusUpdated, PackageStatusUpdated, PackageStatusUpdated method [XPS Documents and Packaging], PackageStatusUpdated method [XPS Documents and Packaging],IPrintDocumentPackageStatusEvent interface, documenttarget/IPrintDocumentPackageStatusEvent::PackageStatusUpdated, xps.iprintdocumentpackagestatusevent_packagestatusupdated
req.header: documenttarget.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPrintDocumentPackageStatusEvent::PackageStatusUpdated
 - documenttarget/IPrintDocumentPackageStatusEvent::PackageStatusUpdated
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Documenttarget.h
api_name:
 - IPrintDocumentPackageStatusEvent.PackageStatusUpdated
---

# IPrintDocumentPackageStatusEvent::PackageStatusUpdated


## -description

Updates the status of the package when the  print job in progress raises an event, or the job completes.

## -parameters

### -param packageStatus [in]

The status update.

## -returns

If the <b>PackageStatusUpdated</b> method completes successfully, it returns an S_OK. Otherwise it returns an appropriate HRESULT  error code.

## -see-also

<a href="/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagestatusevent">IPrintDocumentPackageStatusEvent</a>



<a href="/windows/win32/api/documenttarget/ns-documenttarget-printdocumentpackagestatus">PrintDocumentPackageStatus</a>