---
UID: NF:objbase.CoFreeAllLibraries
title: CoFreeAllLibraries function
author: windows-sdk-content
description: Frees all the DLLs that have been loaded with the CoLoadLibrary function (called internally by CoGetClassObject), regardless of whether they are currently in use.
old-location: com\cofreealllibraries.htm
tech.root: com
ms.assetid: 20616c05-21c6-4895-a1b5-4bae1aa417c7
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: CoFreeAllLibraries, CoFreeAllLibraries function [COM], _com_CoFreeAllLibraries, com.cofreealllibraries, objbase/CoFreeAllLibraries
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - CoFreeAllLibraries
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoFreeAllLibraries function


## -description


Frees all the DLLs that have been loaded with the <a href="https://msdn.microsoft.com/be0d9e82-2438-488e-88c3-68dc7ac3e16f">CoLoadLibrary</a> function (called internally by <a href="https://msdn.microsoft.com/65e758ce-50a4-49e8-b3b2-0cd148d2781a">CoGetClassObject</a>), regardless of whether they are currently in use.


## -parameters






## -returns



This function does not return a value.




## -remarks



To unload libraries, <b>CoFreeAllLibraries</b> uses a list of loaded DLLs for each process that the COM library maintains. The <a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a> and <a href="https://msdn.microsoft.com/b2a8233f-7e1b-4c54-9363-7478c40c3830">OleUninitialize</a> functions call <b>CoFreeAllLibraries</b> internally, so applications usually have no need to call this function directly.





## -see-also




<a href="https://msdn.microsoft.com/3959e7d9-6220-474e-8f85-76f7f935727f">CoFreeLibrary</a>



<a href="https://msdn.microsoft.com/188e9a3b-39cc-454e-af65-4ac797e275d4">CoFreeUnusedLibraries</a>



<a href="https://msdn.microsoft.com/01660e9d-d8f2-40ef-a6d6-b80f0140ab5f">CoFreeUnusedLibrariesEx</a>



<a href="https://msdn.microsoft.com/be0d9e82-2438-488e-88c3-68dc7ac3e16f">CoLoadLibrary</a>
 

 

