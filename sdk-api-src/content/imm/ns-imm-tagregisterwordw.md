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

# tagREGISTERWORDW structure


## -description



Contains reading information or a word to register.




## -struct-fields




### -field lpReading

Pointer to the reading information for the word to register. If the reading information is not needed, the member can be set to <b>NULL</b>.


### -field lpWord

Pointer to the word to register. If a word is not needed, the member can be set to <b>NULL</b>.


## -remarks



The application can pass this structure to the <a href="https://msdn.microsoft.com/acefb3a0-82c7-4af6-8ef0-aba561f570c1">ImmConfigureIME</a> function to have the information or word appear as an initial value in the configuration dialog box for the IME.




## -see-also




<a href="https://msdn.microsoft.com/acefb3a0-82c7-4af6-8ef0-aba561f570c1">ImmConfigureIME</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/1be3ae8b-e083-4420-bc8a-7f49c4264cab">Input Method Manager Structures</a>
 

 

