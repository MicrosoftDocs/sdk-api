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

# IVisualTreeService3::ResolveResource


## -description


Resolves a resource for an element in the tree and applies the resource to the property provided by the specified property index.


## -parameters




### -param resourceContext [in]

The context of the resource.


### -param resourceName [in]

The name of the resource.


### -param resourceType [in]

The type of the resource.


### -param propertyIndex [in]

The index of the property to apply the resource to.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 If no resource was found, or the resource type was invalid, <a href="https://msdn.microsoft.com/F1C11F32-9524-49D6-89DD-C89E4A81720A">IVisualTreeServiceCallback2</a>  will be notified.

Call <a href="https://msdn.microsoft.com/E836FE12-A49A-427C-8013-F1AFBD2C08A2">GetDictionaryItem</a> to get a <i>resourceContext</i> and give better resolution context for <b>ResolveResource</b>.




## -see-also




<a href="https://msdn.microsoft.com/20AD2DC4-388E-458E-AA44-8B2F3464FD6C">IVisualTreeService3</a>
 

 

