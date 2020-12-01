---
UID: NF:xpsobjectmodel_1.IXpsOMObjectFactory1.CreatePageFromStream1
title: IXpsOMObjectFactory1::CreatePageFromStream1 (xpsobjectmodel_1.h)
description: Reads the page markup from the specified stream to create and populate an IXpsOMPage1 interface.
helpviewer_keywords: ["CreatePageFromStream1","CreatePageFromStream1 method [XPS Documents and Packaging]","CreatePageFromStream1 method [XPS Documents and Packaging]","IXpsOMObjectFactory1 interface","IXpsOMObjectFactory1 interface [XPS Documents and Packaging]","CreatePageFromStream1 method","IXpsOMObjectFactory1.CreatePageFromStream1","IXpsOMObjectFactory1::CreatePageFromStream1","xps.ixpsomobjectfactory1_createpagefromstream1","xpsobjectmodel_1/IXpsOMObjectFactory1::CreatePageFromStream1"]
old-location: xps\ixpsomobjectfactory1_createpagefromstream1.htm
tech.root: xps
ms.assetid: 6a400006-0f8f-4eb2-88c0-b559c6a4a0ba
ms.date: 12/05/2018
ms.keywords: CreatePageFromStream1, CreatePageFromStream1 method [XPS Documents and Packaging], CreatePageFromStream1 method [XPS Documents and Packaging],IXpsOMObjectFactory1 interface, IXpsOMObjectFactory1 interface [XPS Documents and Packaging],CreatePageFromStream1 method, IXpsOMObjectFactory1.CreatePageFromStream1, IXpsOMObjectFactory1::CreatePageFromStream1, xps.ixpsomobjectfactory1_createpagefromstream1, xpsobjectmodel_1/IXpsOMObjectFactory1::CreatePageFromStream1
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
 - IXpsOMObjectFactory1::CreatePageFromStream1
 - xpsobjectmodel_1/IXpsOMObjectFactory1::CreatePageFromStream1
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
 - IXpsOMObjectFactory1.CreatePageFromStream1
---

# IXpsOMObjectFactory1::CreatePageFromStream1


## -description

Reads the page markup from the specified stream to create and populate an IXpsOMPage1 interface.

## -parameters

### -param pageMarkupStream

[in]            The stream that contains the page markup.

### -param partUri

[in]            The IOpcPartUri interface that contains the page's URI.

### -param resources

[in]            The IXpsOMPartResources interface that contains the resources used by the page.

### -param reuseObjects

[in]            A Boolean value that indicates that the software is to attempt to optimize the document object tree by sharing objects that are identical in all properties and children. 

TRUE: The software will attempt to optimize the object tree.

FALSE: The software will not attempt to optimize the object tree.

### -param page

[out, retval]   A pointer to the new IXpsOMPage1 interface created by this method. -

## -returns

The method returns an HRESULT. Possible values include, but are not limited to, those in the table that follows. For information about XPS document API return values that are not listed in this table, see XPS Document Errors.

S_OK:  The method succeeded. 

XPS_E_INVALID_CONTENT_TYPE: The image resource type does not match the namespaces used in page markup. For example, one of the elements in the resources collection may be JpegXR but namespaces follow the MSXPS specification. 

E_POINTER: pageMarkupStream, partUri, resources, or page is <b>NULL</b>.

XPS_E_NO_CUSTOM_OBJECTS: resource does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

## -remarks

The IXpsOMPage1 interface returned by this method provides a GetDocumentType method that can be used to identify the XPS document type of the source XML markup in the stream. XPS document type determination is based on the XML namespaces that are used in source markup.

An IXpsOMPage1 interface that contains a document type of XPS_DOCUMENT_TYPE_ OPENXPS can be serialized as a document type of XPS_DOCUMENT_TYPE_ XPS if all of its image resources are compatible with the XPS_DOCUMENT_TYPE_ XPS document format.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1">IXpsOMObjectFactory1</a>