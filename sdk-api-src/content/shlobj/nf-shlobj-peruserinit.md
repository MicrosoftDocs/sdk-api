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

# PerUserInit function


## -description


<p class="CCE_Message">[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Creates <a href="https://msdn.microsoft.com/d9ffda6f-adc0-44a3-b410-e23bf5f4f165">My Documents</a> and other special folders, initializes them as needed, and creates the <b>Send To</b> shortcut menu item for My Documents. 
        


## -parameters






## -returns



This function does not return a value.




## -remarks



Applications do not need to call this function because the operating system already does so.

This function does not have an associated header or library file so it must be called by ordinal value. Call <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> with the DLL name Mydocs.dll to obtain a module handle. Then call <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> with that module handle and the ordinal number 7 to use this function.



