---
UID: NF:xpsobjectmodel_1.IXpsOMObjectFactory1.GetDocumentTypeFromFile
title: IXpsOMObjectFactory1::GetDocumentTypeFromFile
author: windows-sdk-content
description: Detects the type of XPS document that is stored in the specified file.
old-location: xps\ixpsomobjectfactory1_getdocumenttypefromfile.htm
old-project: printdocs
ms.assetid: a122c7cb-4166-46e1-a680-d0644ab8ce81
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetDocumentTypeFromFile, GetDocumentTypeFromFile method [XPS Documents and Packaging], GetDocumentTypeFromFile method [XPS Documents and Packaging],IXpsOMObjectFactory1 interface, IXpsOMObjectFactory1 interface [XPS Documents and Packaging],GetDocumentTypeFromFile method, IXpsOMObjectFactory1.GetDocumentTypeFromFile, IXpsOMObjectFactory1::GetDocumentTypeFromFile, xps.ixpsomobjectfactory1_getdocumenttypefromfile, xpsobjectmodel_1/IXpsOMObjectFactory1::GetDocumentTypeFromFile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel_1.h
req.include-header: 
req.redist: 
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
 - IXpsOMObjectFactory1.GetDocumentTypeFromFile
product: Windows
targetos: Windows
req.lib: None
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMObjectFactory1::GetDocumentTypeFromFile


## -description


Detects the type of XPS document that is stored in the specified file.


## -parameters




### -param filename




### -param documentType

 [out, retval] The document type.


#### - fileName

[in] The name of the  XPS file from which to get the type.


## -returns



Possible values include, but are not limited to, the following. For information about XPS document API return values that are not listed here, see XPS Document Errors.

S_OK: The document type is XPS_DOCUMENT_TYPE_ XPS or XPS_DOCUMENT_TYPE_ OPENXPS. 




## -remarks



This method only parses the data enough to detect the document type. It does not validate the content. A return value of S_OK does not, therefore, imply that the file contains a valid document.




## -see-also




<a href="https://msdn.microsoft.com/f013e59d-83ae-453f-9cc5-9a8230729128">IXpsOMObjectFactory1</a>
 

 

