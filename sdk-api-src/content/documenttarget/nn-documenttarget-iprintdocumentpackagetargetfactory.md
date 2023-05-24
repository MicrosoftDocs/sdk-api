---
UID: NN:documenttarget.IPrintDocumentPackageTargetFactory
title: IPrintDocumentPackageTargetFactory (documenttarget.h)
description: Used with IPrintDocumentPackageTarget for starting a print job.
helpviewer_keywords: ["IPrintDocumentPackageTargetFactory","IPrintDocumentPackageTargetFactory interface [XPS Documents and Packaging]","IPrintDocumentPackageTargetFactory interface [XPS Documents and Packaging]","described","documenttarget/IPrintDocumentPackageTargetFactory","xps.iprintdocumentpackagetargetfactory"]
old-location: xps\iprintdocumentpackagetargetfactory.htm
tech.root: xps
ms.assetid: 631FBF5E-1DDF-49A9-8E1E-201BC6996EA5
ms.date: 12/05/2018
ms.keywords: IPrintDocumentPackageTargetFactory, IPrintDocumentPackageTargetFactory interface [XPS Documents and Packaging], IPrintDocumentPackageTargetFactory interface [XPS Documents and Packaging],described, documenttarget/IPrintDocumentPackageTargetFactory, xps.iprintdocumentpackagetargetfactory
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
 - IPrintDocumentPackageTargetFactory
 - documenttarget/IPrintDocumentPackageTargetFactory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - documenttarget.h
api_name:
 - IPrintDocumentPackageTargetFactory
---

# IPrintDocumentPackageTargetFactory interface

## -description

Used with <a href="/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget">IPrintDocumentPackageTarget</a> for starting a print job.

## -inheritance

The <b>IPrintDocumentPackageTargetFactory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPrintDocumentPackageTargetFactory</b> also has these types of members:

## -members

The <b>IPrintDocumentPackageTargetFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/documenttarget/nf-documenttarget-iprintdocumentpackagetargetfactory-createdocumentpackagetargetforprintjob">CreateDocumentPackageTargetForPrintJob</a>
</td>
<td align="left" width="63%">
Acts as the entry point for creating an <a href="https://docs.microsoft.com/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget">IPrintDocumentPackageTarget</a> object.

</td>
</tr>
</table> 