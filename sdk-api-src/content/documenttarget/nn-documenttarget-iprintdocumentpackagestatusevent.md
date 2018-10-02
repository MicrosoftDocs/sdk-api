---
UID: NN:documenttarget.IPrintDocumentPackageStatusEvent
title: IPrintDocumentPackageStatusEvent
author: windows-sdk-content
description: Represents the progress of the print job.
old-location: xps\iprintdocumentpackagestatusevent.htm
tech.root: printdocs
ms.assetid: A2178E6A-04AD-4024-A083-5C76A5F60743
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IPrintDocumentPackageStatusEvent, IPrintDocumentPackageStatusEvent interface [XPS Documents and Packaging], IPrintDocumentPackageStatusEvent interface [XPS Documents and Packaging],described, documenttarget/IPrintDocumentPackageStatusEvent, xps.iprintdocumentpackagestatusevent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IPrintDocumentPackageStatusEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPrintDocumentPackageStatusEvent interface


## -description


Represents the progress of the print job.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPrintDocumentPackageStatusEvent</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IPrintDocumentPackageStatusEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPrintDocumentPackageStatusEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A672E554-B117-475C-A01E-9FD4EA31621E">PackageStatusUpdated</a>
</td>
<td align="left" width="63%">
Updates the status of the package when the  print job in progress raises an event, or the job completes.

</td>
</tr>
</table> 

