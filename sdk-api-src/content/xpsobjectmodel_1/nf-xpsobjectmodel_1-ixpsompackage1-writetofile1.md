---
UID: NF:xpsobjectmodel_1.IXpsOMPackage1.WriteToFile1
title: IXpsOMPackage1::WriteToFile1 method
author: windows-driver-content
description: Writes an XPS OM to a file as an XPS package of a specified type.
old-location: xps\ixpsompackage1_writetofile1.htm
old-project: printdocs
ms.assetid: 524f951f-5a2b-4ed1-8435-4426739d38f8
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsOMPackage1, IXpsOMPackage1 interface [XPS Documents and Packaging], WriteToFile1 method, IXpsOMPackage1::WriteToFile1, WriteToFile1 method [XPS Documents and Packaging], WriteToFile1 method [XPS Documents and Packaging], IXpsOMPackage1 interface, WriteToFile1,IXpsOMPackage1.WriteToFile1, xps.ixpsompackage1_writetofile1, xpsobjectmodel_1/IXpsOMPackage1::WriteToFile1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xpsobjectmodel_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XPS_DOCUMENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	none
-	none.dll
api_name:
-	IXpsOMPackage1.WriteToFile1
product: Windows
targetos: Windows
req.lib: None
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPackage1::WriteToFile1 method


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
 

 

