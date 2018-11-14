---
UID: NF:combaseapi.CoFreeUnusedLibraries
title: CoFreeUnusedLibraries function
author: windows-sdk-content
description: Unloads any DLLs that are no longer in use, probably because the DLL no longer has any instantiated COM objects outstanding.
old-location: com\cofreeunusedlibraries.htm
tech.root: com
ms.assetid: 188e9a3b-39cc-454e-af65-4ac797e275d4
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CoFreeUnusedLibraries, CoFreeUnusedLibraries function [COM], _com_CoFreeUnusedLibraries, com.cofreeunusedlibraries, combaseapi/CoFreeUnusedLibraries
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoFreeUnusedLibraries
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CoFreeUnusedLibraries
: 
---

# CoFreeUnusedLibraries function


## -description


Unloads any DLLs that are no longer in use, probably because the DLL no longer has any instantiated COM objects outstanding.
<div class="alert"><b>Note</b>  This function is provided for compatibility with 16-bit Windows.</div><div> </div>

## -parameters






## -returns



This function does not return a value.




## -remarks



Applications can call <b>CoFreeUnusedLibraries</b> periodically to free resources. It is most efficient to call it either at the top of a message loop or in some idle-time task. <b>CoFreeUnusedLibraries</b> internally calls <a href="https://msdn.microsoft.com/en-us/library/ms690368(v=VS.85).aspx">DllCanUnloadNow</a> for DLLs that implement and export that function.






## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679758(v=VS.85).aspx">CoFreeAllLibraries</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680658(v=VS.85).aspx">CoFreeLibrary</a>



<a href="https://msdn.microsoft.com/en-us/library/ms678413(v=VS.85).aspx">CoFreeUnusedLibrariesEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692578(v=VS.85).aspx">CoLoadLibrary</a>
 

 

