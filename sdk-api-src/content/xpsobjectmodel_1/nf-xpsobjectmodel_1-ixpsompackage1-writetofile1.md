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

# IXpsOMPackage1::WriteToFile1


## -description


Writes an XPS OM to a file as an XPS package of a specified type.


## -parameters




### -param fileName

[in, string]    The name of the file to be created. This parameter must not be <b>NULL</b>.


### -param securityAttributes

[in, unique]    The SECURITY_ATTRIBUTES structure, which contains two distinct but related data members:

lpSecurityDescriptor: an optional security descriptor

bInheritHandle: a Boolean value that determines whether the returned handle can be inherited by child processes

If lpSecurityDescriptor is <b>NULL</b>, the file or device that is associated with the returned handle will be assigned a default security descriptor. 

For more information about the securityAttributes parameter, refer to CreateFile.


### -param flagsAndAttributes

[in] Specifies the settings and attributes of the file to be created. For most files, a value of FILE_ATTRIBUTE_NORMAL can be used. 

For more information about the flagsAndAttributes parameter, refer to CreateFile.


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

E_INVALIDARG:  The document type was specified as XPS_DOCUMENT_TYPE_UNSPECIFIED.

XPS_E_INVALID_CONTENT_TYPE:  An image resource in the package is of a type that is not supported by the document type specified in documentType. 




## -remarks



The caller must ensure that all image resources in the package are supported by the package type. For example, JpegXR images cannot be used in an MSXPS document type because they are incompatible. 




## -see-also




<a href="https://msdn.microsoft.com/455b7f0b-ade4-4e00-bd9d-836335a7982e">IXpsOMPackage1</a>
 

 

