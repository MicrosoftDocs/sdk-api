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

# tagRECONVERTSTRING structure


## -description



Defines the strings for IME reconversion. It is the first item in a memory block that contains the strings for reconversion.




## -struct-fields




### -field dwSize

Size of this structure and the memory block it heads.


### -field dwVersion

Version number. Must be 0.


### -field dwStrLen

Length of the string that contains the composition string.


### -field dwStrOffset

Offset from the start position of this structure.


### -field dwCompStrLen

Length of the string that will be the composition string.


### -field dwCompStrOffset

Offset of the string that will be the composition string.


### -field dwTargetStrLen

Length of the string that is related to the target clause in the composition string.


### -field dwTargetStrOffset

Offset of the target string.


## -remarks



The <b>dwCompStrOffset</b> and <b>dwTargetOffset</b> members are the relative positions in <b>dwStrOffset</b>. For a Unicode IME, <b>dwStrLen</b>, <b>dwCompStrLen</b>, and <b>dwTargetStrLen</b> are TCHAR values, that is, character counts. The members <b>dwStrOffset</b>, <b>dwCompStrOffset</b>, and <b>dwTargetStrOffset</b> specify byte counts.

If an application starts the reconversion process by calling <a href="https://msdn.microsoft.com/0bac534d-d2a8-4dbc-8062-f1d2a8ca0c34">ImmSetCompositionString</a> with SCS_SETRECONVERTSTRING and SCS_QUERYRECONVERTSTRING, the application must allocate the necessary memory for the <b>RECONVERTSTRING</b> structure as well as the composition string buffer. IME should not use this memory later. If IME starts the process, IME should allocate necessary memory for the structure and the composition string buffer.




## -see-also




<a href="https://msdn.microsoft.com/035a7072-d292-4883-bc3e-d1e9ed64d9ec">IMR_CONFIRMRECONVERTSTRING</a>



<a href="https://msdn.microsoft.com/82ef20b5-bdfa-4bde-abb4-3d14ae35c116">IMR_RECONVERTSTRING</a>



<a href="https://msdn.microsoft.com/0bac534d-d2a8-4dbc-8062-f1d2a8ca0c34">ImmSetCompositionString</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/1be3ae8b-e083-4420-bc8a-7f49c4264cab">Input Method Manager Structures</a>
 

 

