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

# tagMODULEENTRY32W structure


## -description


Describes an entry from a list of the modules belonging to the specified process.


## -struct-fields




### -field dwSize

The size of the structure, in bytes. Before calling the 
<a href="https://msdn.microsoft.com/bb41cab9-13a1-469d-bf76-68c172e982f6">Module32First</a> function, set this member to <code>sizeof(MODULEENTRY32)</code>. If you do not initialize <b>dwSize</b>, 
<b>Module32First</b> fails.


### -field th32ModuleID

This member is no longer used, and is always set to one.


### -field th32ProcessID

The identifier of the process whose modules are to be examined.


### -field GlblcntUsage

The load count of the module, which is not generally meaningful, and usually equal to 0xFFFF.


### -field ProccntUsage

The load count of the module (same as <i>GlblcntUsage</i>), which is not generally meaningful, and usually equal to 0xFFFF.


### -field modBaseAddr

The base address of the module in the context of the owning process.


### -field modBaseSize

The size of the module, in bytes.


### -field hModule

A handle to the module in the context of the owning process.


### -field szModule

The module name.


### -field szExePath

The module path.


## -remarks



The <b>modBaseAddr</b> and <b>hModule</b> members are valid only in the context of the process specified by <i>th32ProcessID</i>.


#### Examples

For an example that uses <b>MODULEENTRY32</b>, see <a href="https://msdn.microsoft.com/8efe1e13-6222-496a-bff3-90f53b03c750">Traversing the Module List</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/bb41cab9-13a1-469d-bf76-68c172e982f6">Module32First</a>



<a href="https://msdn.microsoft.com/88ec1af4-bae7-4cd7-b830-97a98fb337f4">Module32Next</a>
 

 

