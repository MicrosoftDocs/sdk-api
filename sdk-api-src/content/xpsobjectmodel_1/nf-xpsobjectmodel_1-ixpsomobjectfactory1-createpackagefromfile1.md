---
UID: NF:xpsobjectmodel_1.IXpsOMObjectFactory1.CreatePackageFromFile1
title: IXpsOMObjectFactory1::CreatePackageFromFile1 (xpsobjectmodel_1.h)
description: Opens an XPS package file and returns an instantiated XPS document object tree. This method will read a file that contains an XPS document that is of type XPS_DOCUMENT_TYPE_ XPS or XPS_DOCUMENT_TYPE_ OPENXPS.
helpviewer_keywords: ["CreatePackageFromFile1","CreatePackageFromFile1 method [XPS Documents and Packaging]","CreatePackageFromFile1 method [XPS Documents and Packaging]","IXpsOMObjectFactory1 interface","IXpsOMObjectFactory1 interface [XPS Documents and Packaging]","CreatePackageFromFile1 method","IXpsOMObjectFactory1.CreatePackageFromFile1","IXpsOMObjectFactory1::CreatePackageFromFile1","xps.ixpsomobjectfactory1_createpackagefromfile1","xpsobjectmodel_1/IXpsOMObjectFactory1::CreatePackageFromFile1"]
old-location: xps\ixpsomobjectfactory1_createpackagefromfile1.htm
tech.root: xps
ms.assetid: c5641576-9280-48a5-9fb6-ef3d2811386a
ms.date: 12/05/2018
ms.keywords: CreatePackageFromFile1, CreatePackageFromFile1 method [XPS Documents and Packaging], CreatePackageFromFile1 method [XPS Documents and Packaging],IXpsOMObjectFactory1 interface, IXpsOMObjectFactory1 interface [XPS Documents and Packaging],CreatePackageFromFile1 method, IXpsOMObjectFactory1.CreatePackageFromFile1, IXpsOMObjectFactory1::CreatePackageFromFile1, xps.ixpsomobjectfactory1_createpackagefromfile1, xpsobjectmodel_1/IXpsOMObjectFactory1::CreatePackageFromFile1
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
 - IXpsOMObjectFactory1::CreatePackageFromFile1
 - xpsobjectmodel_1/IXpsOMObjectFactory1::CreatePackageFromFile1
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
 - IXpsOMObjectFactory1.CreatePackageFromFile1
---

# IXpsOMObjectFactory1::CreatePackageFromFile1


## -description

Opens an XPS package file and returns an instantiated XPS document object tree. This method will read a file that contains an XPS document that is of type XPS_DOCUMENT_TYPE_ XPS or XPS_DOCUMENT_TYPE_ OPENXPS

## -parameters

### -param filename

[in, string] The name of the XPS package file.

### -param reuseObjects

[in]            The Boolean value that indicates that the software is to attempt to optimize the document object tree by sharing objects that are identical in all properties and children. 

TRUE: The software will attempt to optimize the object tree.

FALSE: The software will not attempt to optimize the object tree.

### -param package

[out, retval]   A pointer to the new IXpsOMPackage1 interface that contains the XPS document object tree that was read from filename.

## -returns

The method returns an HRESULT. Possible values include, but are not limited to, the following. For information about XPS document API return values that are not listed here, see XPS Document Errors.

S_OK: The method succeeded. 

XPS_E_UNEXPECTED_NAMESPACE: The package markup uses a namespace that is not supported by the document type

XPS_E_ABSOLUTE_REFERENCE: The OpenXPS document contains XML elements that use absolute URIs to reference other parts in the document.

## -remarks

Use this method to read a file that contains an XPS document that could be of type XPS_DOCUMENT_TYPE_ XPS or XPS_DOCUMENT_TYPE_ OPENXPS.   <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile">CreatePackageFromFile</a>, released in Windows 7, only opens files that contain an XPS document of type XPS_DOCUMENT_TYPE_ XPS.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1">IXpsOMObjectFactory1</a>