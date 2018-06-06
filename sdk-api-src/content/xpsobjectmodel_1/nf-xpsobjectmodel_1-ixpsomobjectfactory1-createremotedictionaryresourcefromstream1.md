---
UID: NF:xpsobjectmodel_1.IXpsOMObjectFactory1.CreateRemoteDictionaryResourceFromStream1
title: IXpsOMObjectFactory1::CreateRemoteDictionaryResourceFromStream1
author: windows-sdk-content
description: Loads the remote resource dictionary markup into an unrooted IXpsOMRemoteDictionaryResource interface. The dictionary referenced by the dictionaryMarkupStream parameter can contain markup from either the OpenXPS or the MSXPS namespace.
old-location: xps\ixpsomobjectfactory1_createremotedictionaryresourcefromstream1.htm
old-project: printdocs
ms.assetid: e69a139c-511c-43f3-86a3-22aab36f91fc
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: CreateRemoteDictionaryResourceFromStream1, CreateRemoteDictionaryResourceFromStream1 method [XPS Documents and Packaging], CreateRemoteDictionaryResourceFromStream1 method [XPS Documents and Packaging],IXpsOMObjectFactory1 interface, IXpsOMObjectFactory1 interface [XPS Documents and Packaging],CreateRemoteDictionaryResourceFromStream1 method, IXpsOMObjectFactory1.CreateRemoteDictionaryResourceFromStream1, IXpsOMObjectFactory1::CreateRemoteDictionaryResourceFromStream1, xps.ixpsomobjectfactory1_createremotedictionaryresourcefromstream1, xpsobjectmodel_1/IXpsOMObjectFactory1::CreateRemoteDictionaryResourceFromStream1
ms.prod: windows
ms.technology: windows-sdk
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
 - IXpsOMObjectFactory1.CreateRemoteDictionaryResourceFromStream1
product: Windows
targetos: Windows
req.lib: None
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
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
 

 

