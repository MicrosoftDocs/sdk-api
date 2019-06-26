---
UID: NE:documenttarget.PrintDocumentPackageCompletion
title: PrintDocumentPackageCompletion (documenttarget.h)
author: windows-sdk-content
description: The PrintDocumentPackageCompletion enumeration specifies the status of the print operation.
old-location: xps\printdocumentpackagecompletion.htm
tech.root: printdocs
ms.assetid: E8E1F5D3-8CA2-406A-B969-7F5C6F13E064
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PrintDocumentPackageCompletion, PrintDocumentPackageCompletion enumeration [XPS Documents and Packaging], PrintDocumentPackageCompletion_Canceled, PrintDocumentPackageCompletion_Completed, PrintDocumentPackageCompletion_Failed, PrintDocumentPackageCompletion_InProgress, documenttarget/PrintDocumentPackageCompletion, documenttarget/PrintDocumentPackageCompletion_Canceled, documenttarget/PrintDocumentPackageCompletion_Completed, documenttarget/PrintDocumentPackageCompletion_Failed, documenttarget/PrintDocumentPackageCompletion_InProgress, xps.printdocumentpackagecompletion
ms.topic: enum
f1_keywords: 
 - "documenttarget/PrintDocumentPackageCompletion"
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
 - HeaderDef
api_location:
 - Documenttarget.h
api_name:
 - PrintDocumentPackageCompletion
product: Windows
targetos: Windows
req.typenames: PrintDocumentPackageCompletion
req.redist: 
ms.custom: 19H1
---

# PrintDocumentPackageCompletion enumeration


## -description


The PrintDocumentPackageCompletion enumeration specifies the status of the print operation.


## -enum-fields




### -field PrintDocumentPackageCompletion_InProgress

The print job is running.


### -field PrintDocumentPackageCompletion_Completed

The print operation completed without error.


### -field PrintDocumentPackageCompletion_Canceled

The print operation was canceled.


### -field PrintDocumentPackageCompletion_Failed

The print operation failed.

