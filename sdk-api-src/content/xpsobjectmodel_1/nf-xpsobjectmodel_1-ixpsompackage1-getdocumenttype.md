---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

