---
UID: NF:xpsobjectmodel_1.IXpsOMPackage1.GetDocumentType
title: IXpsOMPackage1::GetDocumentType (xpsobjectmodel_1.h)
description: Gets the document type of the data that was used to initialize this package. This method is used to determine whether a document is the XPS or OpenXPS type. For more information, see XPS Documents.
helpviewer_keywords: ["GetDocumentType","GetDocumentType method [XPS Documents and Packaging]","GetDocumentType method [XPS Documents and Packaging]","IXpsOMPackage1 interface","IXpsOMPackage1 interface [XPS Documents and Packaging]","GetDocumentType method","IXpsOMPackage1.GetDocumentType","IXpsOMPackage1::GetDocumentType","xps.ixpsompackage1_getdocumenttype","xpsobjectmodel_1/IXpsOMPackage1::GetDocumentType"]
old-location: xps\ixpsompackage1_getdocumenttype.htm
tech.root: xps
ms.assetid: 8f51e5c5-ac80-4f45-a0bb-ef19137fe391
ms.date: 12/05/2018
ms.keywords: GetDocumentType, GetDocumentType method [XPS Documents and Packaging], GetDocumentType method [XPS Documents and Packaging],IXpsOMPackage1 interface, IXpsOMPackage1 interface [XPS Documents and Packaging],GetDocumentType method, IXpsOMPackage1.GetDocumentType, IXpsOMPackage1::GetDocumentType, xps.ixpsompackage1_getdocumenttype, xpsobjectmodel_1/IXpsOMPackage1::GetDocumentType
req.header: xpsobjectmodel_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: None
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMPackage1::GetDocumentType
 - xpsobjectmodel_1/IXpsOMPackage1::GetDocumentType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - none
 - none.dll
api_name:
 - IXpsOMPackage1.GetDocumentType
---

# IXpsOMPackage1::GetDocumentType


## -description

Gets the document type of the data that was used to initialize this package. This method is used to determine whether a document is the XPS or OpenXPS type. For more information, see <a href="/previous-versions/windows/desktop/dd316975(v=vs.85)">XPS Documents</a>.

## -parameters

### -param documentType

[out, retval] The document type of the source data used to initialize this package. A document type value of XPS_DOCUMENT_TYPE_UNSPECIFIED is returned if the package was created in memory.

## -returns

The method returns an HRESULT. Possible values include, but are not limited to, the following values. For information about XPS Document API return values that are not listed in this table, see XPS Document Errors.

S_OK: The method succeeded.

E_POINTER: documentType is <b>NULL</b>.

## -remarks

If the <a href="/windows/desktop/api/xpsobjectmodel_1/nn-xpsobjectmodel_1-ixpsompackage1">IXpsOMPackage1</a> instance was not loaded from a stream or a  file, the document type is unspecified (XPS_DOCUMENT_TYPE_UNSPECIFIED). Otherwise, the document type returned is that of the stream or file used to initialize the <b>IXpsOMPackage1</b> instance.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel_1/nn-xpsobjectmodel_1-ixpsompackage1">IXpsOMPackage1</a>



<a href="/previous-versions/windows/desktop/dd316975(v=vs.85)">XPS Documents</a>