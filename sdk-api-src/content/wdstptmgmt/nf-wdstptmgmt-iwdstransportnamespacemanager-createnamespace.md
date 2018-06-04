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

# IWdsTransportNamespaceManager::CreateNamespace


## -description


Creates an object of an <a href="https://msdn.microsoft.com/eadb7b1b-aaef-4a4e-a2de-c641a4e10173">IWdsTransportNamespace</a> interface that can be registered on the current WDS transport server.


## -parameters




### -param NamespaceType [in]

The type of the new namespace object. This can be one of the namespace types listed by the <a href="https://msdn.microsoft.com/baba27d2-6df1-4261-b98d-9728ecbb56f2">WDSTRANSPORT_NAMESPACE_TYPE</a> enumeration. 


### -param bszNamespaceName [in]

The name of the new namespace object. If an application attempts to register this namespace with a WDS transport server, WDS confirms that the name is unique. 


### -param bszContentProvider [in]

The name of  the content provider to be associated with the new namespace object.


### -param bszConfiguration [in]

The configuration information used by the content provider. The format of this information is defined by the content provider. The value can be an empty string if no parameter is required.


### -param ppWdsTransportNamespace [out]

A pointer to the object of an <a href="https://msdn.microsoft.com/eadb7b1b-aaef-4a4e-a2de-c641a4e10173">IWdsTransportNamespace</a> interface created by this method. 


## -returns



Standard HRESULT error values are used: S_OK for success; others for failure.




## -see-also




<a href="https://msdn.microsoft.com/eadb7b1b-aaef-4a4e-a2de-c641a4e10173">IWdsTransportNamespace</a>



<a href="https://msdn.microsoft.com/de5fc470-af9f-4f9f-bc17-a347dc702e36">IWdsTransportNamespaceManager</a>



<a href="https://msdn.microsoft.com/baba27d2-6df1-4261-b98d-9728ecbb56f2">WDSTRANSPORT_NAMESPACE_TYPE</a>
 

 

