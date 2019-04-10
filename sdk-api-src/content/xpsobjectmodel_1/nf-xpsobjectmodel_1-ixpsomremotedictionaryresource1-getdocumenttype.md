---
UID: NF:xpsobjectmodel_1.IXpsOMRemoteDictionaryResource1.GetDocumentType
title: IXpsOMRemoteDictionaryResource1::GetDocumentType (xpsobjectmodel_1.h)
author: windows-sdk-content
description: Gets the XPS_DOCUMENT_TYPE of the resource.
old-location: xps\ixpsomremotedictionaryresource1_getdocumenttype.htm
tech.root: printdocs
ms.assetid: C8A55D98-0E3C-448B-9E67-575D5B66535D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDocumentType, GetDocumentType method [XPS Documents and Packaging], GetDocumentType method [XPS Documents and Packaging],IXpsOMRemoteDictionaryResource1 interface, IXpsOMRemoteDictionaryResource1 interface [XPS Documents and Packaging],GetDocumentType method, IXpsOMRemoteDictionaryResource1.GetDocumentType, IXpsOMRemoteDictionaryResource1::GetDocumentType, xps.ixpsomremotedictionaryresource1_getdocumenttype, xpsobjectmodel_1/IXpsOMRemoteDictionaryResource1::GetDocumentType
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
 - IXpsOMRemoteDictionaryResource1.GetDocumentType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMRemoteDictionaryResource1::GetDocumentType


## -description


Gets the <a href="https://msdn.microsoft.com/en-us/library/Hh832138(v=VS.85).aspx">XPS_DOCUMENT_TYPE</a> of the resource.


## -parameters




### -param documentType [out, retval]

The <a href="https://msdn.microsoft.com/en-us/library/Hh832138(v=VS.85).aspx">XPS_DOCUMENT_TYPE</a> document type of the resource.

Returns <a href="https://msdn.microsoft.com/en-us/library/Hh832138(v=VS.85).aspx">XPS_DOCUMENT_TYPE_UNSPECIFIED</a> unless the <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface was created by loading a previously serialized remote dictionary.


## -returns



The method returns an <b>HRESULT</b>.

For information about  XPS document API return values, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.




## -see-also




<a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a>



<a href="https://msdn.microsoft.com/4B8DEDC7-4D7A-408F-9B2B-67B6FC87372F">IXpsOMRemoteDictionaryResource1</a>
 

 

