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

# TTLOADINFO structure


## -description



The <b>TTLOADINFO</b> structure contains the URL from which the embedded font object has been obtained.




## -struct-fields




### -field usStructSize

Size, in bytes, of this structure. The client should set this value to <b>sizeof</b>(TTLOADINFO).


### -field usRefStrSize

Size, in wide characters, of <i>pusRefStr</i>, including the terminating null character.


### -field pusRefStr

Pointer to the string containing the current URL.


## -see-also




<a href="https://msdn.microsoft.com/7e1828bf-c9ed-4120-b91f-b4eb45191e48">TTEMBEDINFO</a>



<a href="https://msdn.microsoft.com/85181d86-bc18-4948-bc7d-65c2d71efefb">TTLoadEmbeddedFont</a>
 

 

