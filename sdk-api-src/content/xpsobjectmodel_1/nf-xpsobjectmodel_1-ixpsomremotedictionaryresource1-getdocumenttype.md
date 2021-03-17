---
UID: NF:xpsobjectmodel_1.IXpsOMRemoteDictionaryResource1.GetDocumentType
title: IXpsOMRemoteDictionaryResource1::GetDocumentType (xpsobjectmodel_1.h)
description: Gets the XPS_DOCUMENT_TYPE of the resource.
helpviewer_keywords: ["GetDocumentType","GetDocumentType method [XPS Documents and Packaging]","GetDocumentType method [XPS Documents and Packaging]","IXpsOMRemoteDictionaryResource1 interface","IXpsOMRemoteDictionaryResource1 interface [XPS Documents and Packaging]","GetDocumentType method","IXpsOMRemoteDictionaryResource1.GetDocumentType","IXpsOMRemoteDictionaryResource1::GetDocumentType","xps.ixpsomremotedictionaryresource1_getdocumenttype","xpsobjectmodel_1/IXpsOMRemoteDictionaryResource1::GetDocumentType"]
old-location: xps\ixpsomremotedictionaryresource1_getdocumenttype.htm
tech.root: xps
ms.assetid: C8A55D98-0E3C-448B-9E67-575D5B66535D
ms.date: 12/05/2018
ms.keywords: GetDocumentType, GetDocumentType method [XPS Documents and Packaging], GetDocumentType method [XPS Documents and Packaging],IXpsOMRemoteDictionaryResource1 interface, IXpsOMRemoteDictionaryResource1 interface [XPS Documents and Packaging],GetDocumentType method, IXpsOMRemoteDictionaryResource1.GetDocumentType, IXpsOMRemoteDictionaryResource1::GetDocumentType, xps.ixpsomremotedictionaryresource1_getdocumenttype, xpsobjectmodel_1/IXpsOMRemoteDictionaryResource1::GetDocumentType
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
 - IXpsOMRemoteDictionaryResource1::GetDocumentType
 - xpsobjectmodel_1/IXpsOMRemoteDictionaryResource1::GetDocumentType
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
 - IXpsOMRemoteDictionaryResource1.GetDocumentType
---

# IXpsOMRemoteDictionaryResource1::GetDocumentType


## -description

Gets the <a href="/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type">XPS_DOCUMENT_TYPE</a> of the resource.

## -parameters

### -param documentType [out, retval]

The <a href="/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type">XPS_DOCUMENT_TYPE</a> document type of the resource.

Returns <a href="/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type">XPS_DOCUMENT_TYPE_UNSPECIFIED</a> unless the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a> interface was created by loading a previously serialized remote dictionary.

## -returns

The method returns an <b>HRESULT</b>.

For information about  XPS document API return values, see <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource">IXpsOMRemoteDictionaryResource</a>



<a href="/windows/desktop/api/xpsobjectmodel_1/nn-xpsobjectmodel_1-ixpsomremotedictionaryresource1">IXpsOMRemoteDictionaryResource1</a>