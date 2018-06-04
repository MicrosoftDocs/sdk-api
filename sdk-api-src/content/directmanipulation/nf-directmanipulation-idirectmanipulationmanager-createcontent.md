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

# IDirectManipulationManager::CreateContent


## -description


The factory method that is used to create an instance of secondary content (such as a panning indicator) inside a viewport.


## -parameters




### -param frameInfo [in, optional]

The frame info provider for the secondary content. This should match the frame info provider used to create the viewport.


### -param clsid [in]

Class identifier (CLSID) of the secondary content. This ID specifies the content type.


### -param riid [in]

IID of the interface.


### -param object [out, retval]

The secondary content object that implements the specified interface.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Primary content is automatically created at the same time as the viewport and has a one-to-one relationship to a viewport. Therefore, it is not possible to create, add, or remove primary content.

Secondary content is created independently from the viewport. There is no limit to how much secondary content can be added or removed from a viewport. All secondary content transforms are derived from those supported by the primary content with specific rules applied based on the intended purpose of the element (identified by its Class identifier (CLSID)).




## -see-also




<a href="https://msdn.microsoft.com/d730a446-984e-4be0-aa7f-6d3dc93b2e34">IDirectManipulationManager</a>
 

 

