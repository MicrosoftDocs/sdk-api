---
UID: NE:winspool.EPrintXPSJobProgress
title: EPrintXPSJobProgress
author: windows-driver-content
description: Specifies what the spooler is currently doing as it processes an XPS print job.
old-location: gdi\eprintxpsjobprogress.htm
old-project: printdocs
ms.assetid: 4fa5b749-e4f9-4f08-97b5-e58f82d0b485
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: EPrintXPSJobProgress, EPrintXPSJobProgress enumeration [Windows GDI], _win32_EPrintXPSJobProgress, gdi.eprintxpsjobprogress, kAddingDocumentSequence, kAddingFixedDocument, kAddingFixedPage, kDocumentSequenceAdded, kFixedDocumentAdded, kFixedPageAdded, kFontAdded, kImageAdded, kResourceAdded, kXpsDocumentCommitted, winspool/EPrintXPSJobProgress, winspool/kAddingDocumentSequence, winspool/kAddingFixedDocument, winspool/kAddingFixedPage, winspool/kDocumentSequenceAdded, winspool/kFixedDocumentAdded, winspool/kFixedPageAdded, winspool/kFontAdded, winspool/kImageAdded, winspool/kResourceAdded, winspool/kXpsDocumentCommitted
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: EPrintXPSJobProgress
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	EPrintXPSJobProgress
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EPrintXPSJobProgress enumeration


## -description


Specifies what the spooler is currently doing as it processes an XPS print job.


## -enum-fields




### -field kAddingDocumentSequence

A document sequence is about to be added to the XPS job.


### -field kDocumentSequenceAdded

A document sequence has been added to the XPS job.


### -field kAddingFixedDocument

A fixed document is about to be added to the XPS job.


### -field kFixedDocumentAdded

A fixed document has been added to the XPS job.


### -field kAddingFixedPage

A page is about to be added to the XPS job.


### -field kFixedPageAdded

A page has been added to the XPS job.


### -field kResourceAdded

A resource had been added to the XPS job.


### -field kFontAdded

A font has been added to the XPS job.


### -field kImageAdded

An image has been added to the XPS job.


### -field kXpsDocumentCommitted

The data for the XPS job has been committed.


## -remarks



This enumeration is primarily used as a parameter for the <a href="https://msdn.microsoft.com/66f7483d-be98-410d-b0c7-430743397de2">ReportJobProcessingProgress</a> function.

These values can refer to either the spooling or the rendering phase of a print job.



