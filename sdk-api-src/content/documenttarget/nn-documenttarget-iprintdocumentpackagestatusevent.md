---
UID: NN:documenttarget.IPrintDocumentPackageStatusEvent
title: IPrintDocumentPackageStatusEvent (documenttarget.h)
description: Represents the progress of the print job.
helpviewer_keywords: ["IPrintDocumentPackageStatusEvent","IPrintDocumentPackageStatusEvent interface [XPS Documents and Packaging]","IPrintDocumentPackageStatusEvent interface [XPS Documents and Packaging]","described","documenttarget/IPrintDocumentPackageStatusEvent","xps.iprintdocumentpackagestatusevent"]
old-location: xps\iprintdocumentpackagestatusevent.htm
tech.root: xps
ms.assetid: A2178E6A-04AD-4024-A083-5C76A5F60743
ms.date: 12/05/2018
ms.keywords: IPrintDocumentPackageStatusEvent, IPrintDocumentPackageStatusEvent interface [XPS Documents and Packaging], IPrintDocumentPackageStatusEvent interface [XPS Documents and Packaging],described, documenttarget/IPrintDocumentPackageStatusEvent, xps.iprintdocumentpackagestatusevent
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
 - IPrintDocumentPackageStatusEvent
 - documenttarget/IPrintDocumentPackageStatusEvent
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
 - IPrintDocumentPackageStatusEvent
---

# IPrintDocumentPackageStatusEvent interface

## -description

Represents the progress of the print job.

## -inheritance

The <b>IPrintDocumentPackageStatusEvent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IPrintDocumentPackageStatusEvent</b> also has these types of members:

## -members

The <b>IPrintDocumentPackageStatusEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/documenttarget/nf-documenttarget-iprintdocumentpackagestatusevent-packagestatusupdated">PackageStatusUpdated</a>
</td>
<td align="left" width="63%">
Updates the status of the package when the  print job in progress raises an event, or the job completes.

</td>
</tr>
</table> 
