---
UID: NF:xpsobjectmodel_1.IXpsOMPackage1.WriteToStream1
title: IXpsOMPackage1::WriteToStream1
author: windows-sdk-content
description: Writes an XPS OM to a stream as an XPS package of a specified type.
old-location: xps\ixpsompackage1_writetostream1.htm
tech.root: printdocs
ms.assetid: 7f430aa1-1570-44d6-9aec-a4b2fb55f2dc
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IXpsOMPackage1 interface [XPS Documents and Packaging],WriteToStream1 method, IXpsOMPackage1.WriteToStream1, IXpsOMPackage1::WriteToStream1, WriteToStream1, WriteToStream1 method [XPS Documents and Packaging], WriteToStream1 method [XPS Documents and Packaging],IXpsOMPackage1 interface, xps.ixpsompackage1_writetostream1, xpsobjectmodel_1/IXpsOMPackage1::WriteToStream1
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IXpsOMPackage1.WriteToStream1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xpsobjectmodel_1.h
: 
- IXpsOMPackage1.WriteToStream1
: 
---

# IXpsOMPackage1::WriteToStream1


## -description


Writes an XPS OM to a stream as an XPS package of a specified type.


## -parameters




### -param outputStream

 [in]            The stream that receives the serialized contents of the package. This parameter must not be <b>NULL</b>.


### -param optimizeMarkupSize

[in]            A Boolean value that indicates whether the document markup will be optimized for size when the contents of the XPS OM are written to the XPS package.

TRUE: The package writer will try to optimize the markup for minimum size.

FALSE: The package writer will not try to perform any optimization.


### -param documentType

[in]            The XPS data format to write to outputStream. The value of this parameter cannot be XPS_DOCUMENT_TYPE_UNSPECIFIED.


## -returns



The method returns an HRESULT. Possible values include, but are not limited to, the following values. For information about XPS Document API return values that are not listed in this table, see XPS Document Errors.

S_OK: The method succeeded.

E_POINTER: documentType is <b>NULL</b>.

E_INVALIDARG: documentType was set to XPS_DOCUMENT_TYPE_UNSPECIFIED.

XPS_E_INVALID_CONTENT_TYPE: An image resource in the package is of a type that is not supported by the document type specified in documentType.




## -see-also




<a href="https://msdn.microsoft.com/455b7f0b-ade4-4e00-bd9d-836335a7982e">IXpsOMPackage1</a>
 

 

