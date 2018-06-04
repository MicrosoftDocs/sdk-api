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

# IXpsOMRemoteDictionaryResource1::GetDocumentType


## -description


Gets the <a href="https://msdn.microsoft.com/C34629CB-7F8C-4126-BBE3-BF506D7586E9">XPS_DOCUMENT_TYPE</a> of the resource.


## -parameters




### -param documentType [out, retval]

The <a href="https://msdn.microsoft.com/C34629CB-7F8C-4126-BBE3-BF506D7586E9">XPS_DOCUMENT_TYPE</a> document type of the resource.

Returns <a href="https://msdn.microsoft.com/C34629CB-7F8C-4126-BBE3-BF506D7586E9">XPS_DOCUMENT_TYPE_UNSPECIFIED</a> unless the <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface was created by loading a previously serialized remote dictionary.


## -returns



The method returns an <b>HRESULT</b>.

For information about  XPS document API return values, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.




## -see-also




<a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a>



<a href="https://msdn.microsoft.com/4B8DEDC7-4D7A-408F-9B2B-67B6FC87372F">IXpsOMRemoteDictionaryResource1</a>
 

 

