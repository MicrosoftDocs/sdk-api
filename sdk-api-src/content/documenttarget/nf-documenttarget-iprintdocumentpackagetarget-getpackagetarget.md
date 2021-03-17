---
UID: NF:documenttarget.IPrintDocumentPackageTarget.GetPackageTarget
title: IPrintDocumentPackageTarget::GetPackageTarget (documenttarget.h)
description: Retrieves the pointer to the specific document package target, which allows the client to add a document with the given target type. Clients can call this method multiple times but they always have to use the same target ID.
helpviewer_keywords: ["GetPackageTarget","GetPackageTarget method [XPS Documents and Packaging]","GetPackageTarget method [XPS Documents and Packaging]","IPrintDocumentPackageTarget interface","IPrintDocumentPackageTarget interface [XPS Documents and Packaging]","GetPackageTarget method","IPrintDocumentPackageTarget.GetPackageTarget","IPrintDocumentPackageTarget::GetPackageTarget","documenttarget/IPrintDocumentPackageTarget::GetPackageTarget","xps.iprintdocumentpackagetarget_getpackagetarget"]
old-location: xps\iprintdocumentpackagetarget_getpackagetarget.htm
tech.root: xps
ms.assetid: 7D9A749D-954E-43BA-A522-98CBAD79D18C
ms.date: 12/05/2018
ms.keywords: GetPackageTarget, GetPackageTarget method [XPS Documents and Packaging], GetPackageTarget method [XPS Documents and Packaging],IPrintDocumentPackageTarget interface, IPrintDocumentPackageTarget interface [XPS Documents and Packaging],GetPackageTarget method, IPrintDocumentPackageTarget.GetPackageTarget, IPrintDocumentPackageTarget::GetPackageTarget, documenttarget/IPrintDocumentPackageTarget::GetPackageTarget, xps.iprintdocumentpackagetarget_getpackagetarget
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
 - IPrintDocumentPackageTarget::GetPackageTarget
 - documenttarget/IPrintDocumentPackageTarget::GetPackageTarget
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
 - IPrintDocumentPackageTarget.GetPackageTarget
---

# IPrintDocumentPackageTarget::GetPackageTarget


## -description

Retrieves the pointer to the specific document package target, which allows the client to add a document with the given target type. Clients can call this method multiple times but they always have to use  the same target ID.

## -parameters

### -param guidTargetType [in]

The target type GUID obtained from <a href="/windows/desktop/api/documenttarget/nf-documenttarget-iprintdocumentpackagetarget-getpackagetargettypes">GetPackageTargetTypes</a>.

### -param riid [in]

The identifier of the interface being requested.

### -param ppvTarget [out]

The requested document target interface. The returned pointer is a pointer to an <a href="/windows/desktop/api/xpsobjectmodel_1/nn-xpsobjectmodel_1-ixpsdocumentpackagetarget">IXpsDocumentPackageTarget</a> interface.

## -returns

If the <b>GetPackageTarget</b> method completes successfully, it returns an S_OK. Otherwise it returns the appropriate HRESULT error code.

## -see-also

<a href="/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget">IPrintDocumentPackageTarget</a>