---
UID: NF:xpsobjectmodel_1.IXpsOMPackage1.WriteToFile1
title: IXpsOMPackage1::WriteToFile1 (xpsobjectmodel_1.h)
description: Writes an XPS OM to a file as an XPS package of a specified type.
helpviewer_keywords: ["IXpsOMPackage1 interface [XPS Documents and Packaging]","WriteToFile1 method","IXpsOMPackage1.WriteToFile1","IXpsOMPackage1::WriteToFile1","WriteToFile1","WriteToFile1 method [XPS Documents and Packaging]","WriteToFile1 method [XPS Documents and Packaging]","IXpsOMPackage1 interface","xps.ixpsompackage1_writetofile1","xpsobjectmodel_1/IXpsOMPackage1::WriteToFile1"]
old-location: xps\ixpsompackage1_writetofile1.htm
tech.root: xps
ms.assetid: 524f951f-5a2b-4ed1-8435-4426739d38f8
ms.date: 12/05/2018
ms.keywords: IXpsOMPackage1 interface [XPS Documents and Packaging],WriteToFile1 method, IXpsOMPackage1.WriteToFile1, IXpsOMPackage1::WriteToFile1, WriteToFile1, WriteToFile1 method [XPS Documents and Packaging], WriteToFile1 method [XPS Documents and Packaging],IXpsOMPackage1 interface, xps.ixpsompackage1_writetofile1, xpsobjectmodel_1/IXpsOMPackage1::WriteToFile1
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
 - IXpsOMPackage1::WriteToFile1
 - xpsobjectmodel_1/IXpsOMPackage1::WriteToFile1
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
 - IXpsOMPackage1.WriteToFile1
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

<a href="/windows/desktop/api/xpsobjectmodel_1/nn-xpsobjectmodel_1-ixpsompackage1">IXpsOMPackage1</a>