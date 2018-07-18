---
UID: NF:xpsobjectmodel_1.IXpsOMPackage1.GetDocumentType
title: IXpsOMPackage1::GetDocumentType
author: windows-sdk-content
description: Gets the document type of the data that was used to initialize this package. This method is used to determine whether a document is the XPS or OpenXPS type. For more information, see XPS Documents.
old-location: xps\ixpsompackage1_getdocumenttype.htm
old-project: printdocs
ms.assetid: 8f51e5c5-ac80-4f45-a0bb-ef19137fe391
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetDocumentType, GetDocumentType method [XPS Documents and Packaging], GetDocumentType method [XPS Documents and Packaging],IXpsOMPackage1 interface, IXpsOMPackage1 interface [XPS Documents and Packaging],GetDocumentType method, IXpsOMPackage1.GetDocumentType, IXpsOMPackage1::GetDocumentType, xps.ixpsompackage1_getdocumenttype, xpsobjectmodel_1/IXpsOMPackage1::GetDocumentType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: XPS_DOCUMENT_TYPE
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
product: Windows
targetos: Windows
req.lib: None
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPackage1::GetDocumentType


## -description


Gets the document type of the data that was used to initialize this package. This method is used to determine whether a document is the XPS or OpenXPS type. For more information, see <a href="https://msdn.microsoft.com/14ae2c97-8596-46db-a55c-ef706d2cd00b">XPS Documents</a>.


## -parameters




### -param documentType

[out, retval] The document type of the source data used to initialize this package. A document type value of XPS_DOCUMENT_TYPE_UNSPECIFIED is returned if the package was created in memory.


## -returns



The method returns an HRESULT. Possible values include, but are not limited to, the following values. For information about XPS Document API return values that are not listed in this table, see XPS Document Errors.

S_OK: The method succeeded.

E_POINTER: documentType is <b>NULL</b>.




## -remarks



If the <a href="https://msdn.microsoft.com/455b7f0b-ade4-4e00-bd9d-836335a7982e">IXpsOMPackage1</a> instance was not loaded from a stream or a  file, the document type is unspecified (XPS_DOCUMENT_TYPE_UNSPECIFIED). Otherwise, the document type returned is that of the stream or file used to initialize the <b>IXpsOMPackage1</b> instance.




## -see-also




<a href="https://msdn.microsoft.com/455b7f0b-ade4-4e00-bd9d-836335a7982e">IXpsOMPackage1</a>



<a href="https://msdn.microsoft.com/14ae2c97-8596-46db-a55c-ef706d2cd00b">XPS Documents</a>
 

 

