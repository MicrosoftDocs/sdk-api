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

# UnmapDebugInformation function


## -description


Deallocates the memory and resources allocated by a call to the 
<a href="https://msdn.microsoft.com/749a2a99-f6c4-4af3-aa0b-8a7bb5c690da">MapDebugInformation</a> function.
<div class="alert"><b>Note</b>  This function is provided only for backward compatibility. New applications should use the 
<a href="https://msdn.microsoft.com/f4801039-eba2-4ec3-8c23-706ab89bb442">SymUnloadModule64</a> function.</div><div> </div>

## -parameters




### -param DebugInfo [in]

A pointer to an 
<a href="https://msdn.microsoft.com/f8db7695-4967-45c0-a6bf-019e825bd9ab">IMAGE_DEBUG_INFORMATION</a> structure that is returned from a call to 
<a href="https://msdn.microsoft.com/749a2a99-f6c4-4af3-aa0b-8a7bb5c690da">MapDebugInformation</a>.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>UnmapDebugInformation</b> function is the counterpart to the 
<a href="https://msdn.microsoft.com/749a2a99-f6c4-4af3-aa0b-8a7bb5c690da">MapDebugInformation</a> function and must be used to deallocate the memory and resources allocated by a call to the 
<a href="https://msdn.microsoft.com/749a2a99-f6c4-4af3-aa0b-8a7bb5c690da">MapDebugInformation</a> function.
			

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/f8db7695-4967-45c0-a6bf-019e825bd9ab">IMAGE_DEBUG_INFORMATION</a>



<a href="https://msdn.microsoft.com/749a2a99-f6c4-4af3-aa0b-8a7bb5c690da">MapDebugInformation</a>
 

 

