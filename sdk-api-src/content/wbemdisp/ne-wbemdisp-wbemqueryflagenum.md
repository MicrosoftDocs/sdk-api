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

# WbemQueryFlagEnum enumeration


## -description


The 
<b>WbemQueryFlagEnum</b> constants define the depth of enumeration or query, which determines how many objects are returned by a call. These constants are used by 
<a href="https://msdn.microsoft.com/cfe08956-7215-4e2e-a279-6e86f14e5c27">SWbemServices.SubclassesOf</a>, 
<a href="https://msdn.microsoft.com/6465a981-f98e-4ece-a9b6-9da8ae618bc6">SWbemServices.InstancesOf</a>, 
<a href="https://msdn.microsoft.com/c17e5d4a-016f-42ae-bc11-e21a44772ce5">SWbemObject.Subclasses_</a>, and 
<a href="https://msdn.microsoft.com/30402d7d-f7cb-43b5-96b5-a8a76144e32d">SWbemObject.Instances_</a>.

The WMI scripting type library, wbemdisp.tlb, defines these constants. Visual Basic applications can access this library; script languages must use the value of the constant directly, unless they use Windows Script Host (WSH) XML file format. For more information, see 
<a href="https://msdn.microsoft.com/6ef4e210-0733-4f2a-89c1-1a7aca5a19d9">Using the WMI Scripting Type Library</a>.


## -enum-fields




### -field wbemQueryFlagDeep

Forces recursive enumeration into all subclasses derived from the specified parent class. The parent class itself is not returned in the enumeration.


### -field wbemQueryFlagShallow

Forces the enumeration to include only immediate subclasses of the specified parent class.


### -field wbemQueryFlagPrototype

Used for prototyping. It stops the query from happening and instead returns an object that look like a typical result object.


## -see-also




<a href="https://msdn.microsoft.com/feaab757-3167-420b-8f42-edced4cd4c53">Scripting API Constants</a>
 

 

