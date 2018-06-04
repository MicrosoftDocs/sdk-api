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

# IXpsOMObjectFactory1::CreateRemoteDictionaryResourceFromStream1


## -description


Loads the remote resource dictionary markup into an unrooted IXpsOMRemoteDictionaryResource interface. The dictionary referenced by the dictionaryMarkupStream parameter can contain markup from either the OpenXPS or the MSXPS namespace. 


## -parameters




### -param dictionaryMarkupStream

[in]            The IStream interface that contains the remote resource dictionary markup.


### -param partUri

[in]            The IOpcPartUri interface that contains the part name to be assigned to this resource.


### -param resources

The IXpsOMPartResources interface for the part resources of the dictionary resource objects that have streams.


### -param dictionaryResource

[in]            A pointer to the new IXpsOMRemoteDictionaryResource interface.


## -returns



The method returns an HRESULT. Possible values include, but are not limited to, those in the table that follows. For information about XPS document API return values that are not listed in this table, see XPS Document Errors. 

S_OK: The method succeeded.

XPS_E_INVALID_CONTENT_TYPE: An image resource type does not match the namespaces used in the markup. For example, if one of the elements in resources may be JpegXR but namespaces follow the MSXPS specification. 

E_POINTER: dictionaryMarkupStream, dictionaryPartUri, resources, or dictionaryResource is <b>NULL</b>.

XPS_E_NO_CUSTOM_OBJECTS: resource does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.




## -remarks



Use this method to create a remote dictionary from a stream whose contents could be of type XPS_DOCUMENT_TYPE_ XPS or XPS_DOCUMENT_TYPE_ OPENXPS.   CreateRemoteDictionaryResourceFromStream, released in Windows 7, only reads streams of type XPS_DOCUMENT_TYPE_ XPS.




## -see-also




<a href="https://msdn.microsoft.com/f013e59d-83ae-453f-9cc5-9a8230729128">IXpsOMObjectFactory1</a>
 

 

