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

# tagOLEVERB structure


## -description


Defines a verb that an object supports. The <a href="https://msdn.microsoft.com/c67770d0-e478-41dc-9028-1e0a6cb9e3c7">IOleObject::EnumVerbs</a> method creates an enumerator that can enumerate these structures for an object, and supplies a pointer to the enumerator's <a href="https://msdn.microsoft.com/fc9b3474-6f56-4274-af7d-72e0920c0457">IEnumOLEVERB</a>.


## -struct-fields




### -field lVerb

Integer identifier associated with this verb.


### -field lpszVerbName

Pointer to a string that contains the verb's name.


### -field fuFlags

In Windows, a group of flags taken from the flag constants beginning with MF_ defined in <a href="_win32_AppendMenu">AppendMenu</a>. Containers should use these flags in building an object's verb menu. All Flags defined in <b>AppendMenu</b> are supported except for MF_BITMAP, MF_OWNERDRAW, and MF_POPUP.


### -field grfAttribs

Combination of the verb attributes in the <a href="https://msdn.microsoft.com/797498ba-5ad6-4476-87d8-de85b30396f4">OLEVERBATTRIB</a> enumeration.



## -see-also




<a href="https://msdn.microsoft.com/fc9b3474-6f56-4274-af7d-72e0920c0457">IEnumOLEVERB</a>



<a href="https://msdn.microsoft.com/c67770d0-e478-41dc-9028-1e0a6cb9e3c7">IOleObject::EnumVerbs</a>
 

 

