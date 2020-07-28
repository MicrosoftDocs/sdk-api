---
UID: NF:xpsobjectmodel_1.IXpsOMObjectFactory1.GetDocumentTypeFromFile
title: IXpsOMObjectFactory1::GetDocumentTypeFromFile (xpsobjectmodel_1.h)
description: Detects the type of XPS document that is stored in the specified file.
helpviewer_keywords: ["GetDocumentTypeFromFile","GetDocumentTypeFromFile method [XPS Documents and Packaging]","GetDocumentTypeFromFile method [XPS Documents and Packaging]","IXpsOMObjectFactory1 interface","IXpsOMObjectFactory1 interface [XPS Documents and Packaging]","GetDocumentTypeFromFile method","IXpsOMObjectFactory1.GetDocumentTypeFromFile","IXpsOMObjectFactory1::GetDocumentTypeFromFile","xps.ixpsomobjectfactory1_getdocumenttypefromfile","xpsobjectmodel_1/IXpsOMObjectFactory1::GetDocumentTypeFromFile"]
old-location: xps\ixpsomobjectfactory1_getdocumenttypefromfile.htm
tech.root: xps
ms.assetid: a122c7cb-4166-46e1-a680-d0644ab8ce81
ms.date: 12/05/2018
ms.keywords: GetDocumentTypeFromFile, GetDocumentTypeFromFile method [XPS Documents and Packaging], GetDocumentTypeFromFile method [XPS Documents and Packaging],IXpsOMObjectFactory1 interface, IXpsOMObjectFactory1 interface [XPS Documents and Packaging],GetDocumentTypeFromFile method, IXpsOMObjectFactory1.GetDocumentTypeFromFile, IXpsOMObjectFactory1::GetDocumentTypeFromFile, xps.ixpsomobjectfactory1_getdocumenttypefromfile, xpsobjectmodel_1/IXpsOMObjectFactory1::GetDocumentTypeFromFile
f1_keywords:
- xpsobjectmodel_1/IXpsOMObjectFactory1.GetDocumentTypeFromFile
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- none
- none.dll
api_name:
- IXpsOMObjectFactory1.GetDocumentTypeFromFile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMObjectFactory1::GetDocumentTypeFromFile


## -description


Detects the type of XPS document that is stored in the specified file.


## -parameters




### -param filename

[in] The name of the  XPS file from which to get the type.


### -param documentType

 [out, retval] The document type.


## -returns



Possible values include, but are not limited to, the following. For information about XPS document API return values that are not listed here, see XPS Document Errors.

S_OK: The document type is XPS_DOCUMENT_TYPE_ XPS or XPS_DOCUMENT_TYPE_ OPENXPS. 




## -remarks



This method only parses the data enough to detect the document type. It does not validate the content. A return value of S_OK does not, therefore, imply that the file contains a valid document.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1">IXpsOMObjectFactory1</a>
 

 

