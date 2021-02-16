---
UID: NF:xpsobjectmodel_1.IXpsOMObjectFactory1.GetDocumentTypeFromStream
title: IXpsOMObjectFactory1::GetDocumentTypeFromStream (xpsobjectmodel_1.h)
description: Detects the type of XPS document that is stored in the specified stream.
helpviewer_keywords: ["GetDocumentTypeFromStream","GetDocumentTypeFromStream method [XPS Documents and Packaging]","GetDocumentTypeFromStream method [XPS Documents and Packaging]","IXpsOMObjectFactory1 interface","IXpsOMObjectFactory1 interface [XPS Documents and Packaging]","GetDocumentTypeFromStream method","IXpsOMObjectFactory1.GetDocumentTypeFromStream","IXpsOMObjectFactory1::GetDocumentTypeFromStream","xps.ixpsomobjectfactory1_getdocumenttypefromstream","xpsobjectmodel_1/IXpsOMObjectFactory1::GetDocumentTypeFromStream"]
old-location: xps\ixpsomobjectfactory1_getdocumenttypefromstream.htm
tech.root: xps
ms.assetid: 98d5bfc1-75f7-425f-b69d-11e74c15f08e
ms.date: 12/05/2018
ms.keywords: GetDocumentTypeFromStream, GetDocumentTypeFromStream method [XPS Documents and Packaging], GetDocumentTypeFromStream method [XPS Documents and Packaging],IXpsOMObjectFactory1 interface, IXpsOMObjectFactory1 interface [XPS Documents and Packaging],GetDocumentTypeFromStream method, IXpsOMObjectFactory1.GetDocumentTypeFromStream, IXpsOMObjectFactory1::GetDocumentTypeFromStream, xps.ixpsomobjectfactory1_getdocumenttypefromstream, xpsobjectmodel_1/IXpsOMObjectFactory1::GetDocumentTypeFromStream
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
 - IXpsOMObjectFactory1::GetDocumentTypeFromStream
 - xpsobjectmodel_1/IXpsOMObjectFactory1::GetDocumentTypeFromStream
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
 - IXpsOMObjectFactory1.GetDocumentTypeFromStream
---

# IXpsOMObjectFactory1::GetDocumentTypeFromStream


## -description

Detects the type of XPS document that is stored in the specified stream.

## -parameters

### -param xpsDocumentStream

[in] A stream that contains XPS OM data. The stream must support sequential reading and the read position of the stream must be set to the beginning of the XPS data.

### -param documentType

[out, retval] The document type of the XPS data found in the stream.

## -returns

Possible values include, but are not limited to, the following. For information about XPS document API return values that are not listed here, see XPS Document Errors.

S_OK: The document type is XPS_DOCUMENT_TYPE_ XPS or XPS_DOCUMENT_TYPE_ OPENXPS.

## -remarks

This method only parses the data enough to detect the document type. It does not validate the content. A return value of S_OK does not, therefore, imply that the stream contains a valid document.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1">IXpsOMObjectFactory1</a>