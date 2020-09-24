---
UID: NF:xpsobjectmodel_1.IXpsDocumentPackageTarget.GetXpsOMPackageWriter
title: IXpsDocumentPackageTarget::GetXpsOMPackageWriter (xpsobjectmodel_1.h)
description: Gets the IXpsOMPackageWriter object for the document package.
helpviewer_keywords: ["GetXpsOMPackageWriter","GetXpsOMPackageWriter method [XPS Documents and Packaging]","GetXpsOMPackageWriter method [XPS Documents and Packaging]","IXpsDocumentPackageTarget interface","IXpsDocumentPackageTarget interface [XPS Documents and Packaging]","GetXpsOMPackageWriter method","IXpsDocumentPackageTarget.GetXpsOMPackageWriter","IXpsDocumentPackageTarget::GetXpsOMPackageWriter","xps.ixpsdocumentpackagetarget_getxpsompackagewriter","xpsobjectmodel_1/IXpsDocumentPackageTarget::GetXpsOMPackageWriter"]
old-location: xps\ixpsdocumentpackagetarget_getxpsompackagewriter.htm
tech.root: xps
ms.assetid: D20AE05F-466F-44B6-972A-06AA872FF7BA
ms.date: 12/05/2018
ms.keywords: GetXpsOMPackageWriter, GetXpsOMPackageWriter method [XPS Documents and Packaging], GetXpsOMPackageWriter method [XPS Documents and Packaging],IXpsDocumentPackageTarget interface, IXpsDocumentPackageTarget interface [XPS Documents and Packaging],GetXpsOMPackageWriter method, IXpsDocumentPackageTarget.GetXpsOMPackageWriter, IXpsDocumentPackageTarget::GetXpsOMPackageWriter, xps.ixpsdocumentpackagetarget_getxpsompackagewriter, xpsobjectmodel_1/IXpsDocumentPackageTarget::GetXpsOMPackageWriter
req.header: xpsobjectmodel_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Xpsobjectmodel_1.idl
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
 - IXpsDocumentPackageTarget::GetXpsOMPackageWriter
 - xpsobjectmodel_1/IXpsDocumentPackageTarget::GetXpsOMPackageWriter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xpsobjectmodel_1.h
api_name:
 - IXpsDocumentPackageTarget.GetXpsOMPackageWriter
---

# IXpsDocumentPackageTarget::GetXpsOMPackageWriter


## -description

Gets the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a> object for the document package.

## -parameters

### -param documentSequencePartName [in]

The document sequence part name.

### -param discardControlPartName [in]

The control part name.

### -param packageWriter [out, retval]

The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a> object.

## -returns

This method returns an HRESULT value. If the method call fails, it returns the appropriate HRESULT error code.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel_1/nn-xpsobjectmodel_1-ixpsdocumentpackagetarget">IXpsDocumentPackageTarget</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a>