---
UID: NN:documenttarget.IPrintDocumentPackageTarget
title: IPrintDocumentPackageTarget (documenttarget.h)
description: Allows users to enumerate the supported package target types and to create one with a given type ID. IPrintDocumentPackageTarget also supports the tracking of the package printing progress and cancelling.
helpviewer_keywords: ["IPrintDocumentPackageTarget","IPrintDocumentPackageTarget interface [XPS Documents and Packaging]","IPrintDocumentPackageTarget interface [XPS Documents and Packaging]","described","documenttarget/IPrintDocumentPackageTarget","xps.iprintdocumentpackagetarget"]
old-location: xps\iprintdocumentpackagetarget.htm
tech.root: xps
ms.assetid: 0F63C626-DB58-4952-BBB3-7E3901429C35
ms.date: 12/05/2018
ms.keywords: IPrintDocumentPackageTarget, IPrintDocumentPackageTarget interface [XPS Documents and Packaging], IPrintDocumentPackageTarget interface [XPS Documents and Packaging],described, documenttarget/IPrintDocumentPackageTarget, xps.iprintdocumentpackagetarget
req.header: documenttarget.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IPrintDocumentPackageTarget
 - documenttarget/IPrintDocumentPackageTarget
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
 - IPrintDocumentPackageTarget
---

# IPrintDocumentPackageTarget interface

## -description

Allows users to enumerate the supported package target types and to create one with a given type ID. <b>IPrintDocumentPackageTarget</b> also supports the tracking of the package printing progress and cancelling.

## -inheritance

The <b>IPrintDocumentPackageTarget</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPrintDocumentPackageTarget</b> also has these types of members:

## -members

The <b>IPrintDocumentPackageTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/documenttarget/nf-documenttarget-iprintdocumentpackagetarget-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels the current print job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/documenttarget/nf-documenttarget-iprintdocumentpackagetarget-getpackagetarget">GetPackageTarget</a>
</td>
<td align="left" width="63%">
Retrieves the pointer to the specific document package target, which allows the client to add a document with the given target type. Clients can call this method multiple times but they always have to use  the same target ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/documenttarget/nf-documenttarget-iprintdocumentpackagetarget-getpackagetargettypes">GetPackageTargetTypes</a>
</td>
<td align="left" width="63%">
Enumerates the supported target types.

</td>
</tr>
</table> 