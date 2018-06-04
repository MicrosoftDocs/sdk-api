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

# IXpsOMObjectFactory1::CreatePageFromStream1


## -description


Reads the page markup from the specified stream to create and populate an IXpsOMPage1 interface.


## -parameters




### -param pageMarkupStream

[in]            The stream that contains the page markup.


### -param partUri

[in]            The IOpcPartUri interface that contains the page's URI.


### -param resources

[in]            The IXpsOMPartResources interface that contains the resources used by the page.


### -param reuseObjects

[in]            A Boolean value that indicates that the software is to attempt to optimize the document object tree by sharing objects that are identical in all properties and children. 

TRUE: The software will attempt to optimize the object tree.

FALSE: The software will not attempt to optimize the object tree.


### -param page

[out, retval]   A pointer to the new IXpsOMPage1 interface created by this method. - 


## -returns



The method returns an HRESULT. Possible values include, but are not limited to, those in the table that follows. For information about XPS document API return values that are not listed in this table, see XPS Document Errors.

S_OK:  The method succeeded. 

XPS_E_INVALID_CONTENT_TYPE: The image resource type does not match the namespaces used in page markup. For example, one of the elements in the resources collection may be JpegXR but namespaces follow the MSXPS specification. 

E_POINTER: pageMarkupStream, partUri, resources, or page is <b>NULL</b>.

XPS_E_NO_CUSTOM_OBJECTS: resource does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.




## -remarks



The IXpsOMPage1 interface returned by this method provides a GetDocumentType method that can be used to identify the XPS document type of the source XML markup in the stream. XPS document type determination is based on the XML namespaces that are used in source markup.

An IXpsOMPage1 interface that contains a document type of XPS_DOCUMENT_TYPE_ OPENXPS can be serialized as a document type of XPS_DOCUMENT_TYPE_ XPS if all of its image resources are compatible with the XPS_DOCUMENT_TYPE_ XPS document format.




## -see-also




<a href="https://msdn.microsoft.com/f013e59d-83ae-453f-9cc5-9a8230729128">IXpsOMObjectFactory1</a>
 

 

