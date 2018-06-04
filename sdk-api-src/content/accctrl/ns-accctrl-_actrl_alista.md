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

# _ACTRL_ALISTA structure


## -description


Contains an array of access-control lists for an object and its properties.


## -struct-fields




### -field cEntries

The number of entries in the <b>pPropertyAccessList</b> array.


### -field pPropertyAccessList

An array of <a href="https://msdn.microsoft.com/90b13dd1-0ca6-4674-b9fa-a61aed4637d7">ACTRL_PROPERTY_ENTRY</a> structures. Each structure contains a list of access-control entries for an object or a specified property on the object.


### -field pPropertyAccessList.size_is

 


### -field pPropertyAccessList.size_is.cEntries

 




## -remarks



Note the following type definition.

<pre class="syntax" xml:space="preserve"><code>typedef PACTRL_ACCESSW PACTRL_ACCESSW_ALLOCATE_ALL_NODES;</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/f8ec6743-633b-4c79-afac-68eb20e07b2a">IAccessControl::GrantAccessRights</a>
 

 

