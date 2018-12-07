---
UID: NF:documenttarget.IPrintDocumentPackageStatusEvent.PackageStatusUpdated
title: IPrintDocumentPackageStatusEvent::PackageStatusUpdated
author: windows-sdk-content
description: Updates the status of the package when the print job in progress raises an event, or the job completes.
old-location: xps\iprintdocumentpackagestatusevent_packagestatusupdated.htm
tech.root: printdocs
ms.assetid: A672E554-B117-475C-A01E-9FD4EA31621E
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPrintDocumentPackageStatusEvent interface [XPS Documents and Packaging],PackageStatusUpdated method, IPrintDocumentPackageStatusEvent.PackageStatusUpdated, IPrintDocumentPackageStatusEvent::PackageStatusUpdated, PackageStatusUpdated, PackageStatusUpdated method [XPS Documents and Packaging], PackageStatusUpdated method [XPS Documents and Packaging],IPrintDocumentPackageStatusEvent interface, documenttarget/IPrintDocumentPackageStatusEvent::PackageStatusUpdated, xps.iprintdocumentpackagestatusevent_packagestatusupdated
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Documenttarget.h
api_name:
 - IPrintDocumentPackageStatusEvent.PackageStatusUpdated
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/A2178E6A-04AD-4024-A083-5C76A5F60743">IPrintDocumentPackageStatusEvent</a>



<a href="https://msdn.microsoft.com/A499CB8D-B2E3-4343-A9AF-079C75EF1441">PrintDocumentPackageStatus</a>
 

 

