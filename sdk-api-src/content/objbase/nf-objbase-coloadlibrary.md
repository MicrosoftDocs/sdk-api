---
UID: NF:objbase.CoLoadLibrary
title: CoLoadLibrary function
author: windows-driver-content
description: Loads a specific DLL into the caller's process.
old-location: com\coloadlibrary.htm
old-project: com
ms.assetid: be0d9e82-2438-488e-88c3-68dc7ac3e16f
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: CoLoadLibrary, CoLoadLibrary function [COM], _com_CoLoadLibrary, com.coloadlibrary, objbase/CoLoadLibrary
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
req.typenames: COMSD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ole32.dll
api_name:
-	CoLoadLibrary
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# CoLoadLibrary function


## -description


Loads a specific DLL into the caller's process.

<b>CoLoadLibrary</b> is equivalent to <a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a>. <b>CoLoadLibrary</b> does not affect the lifetime of the library. 



## -parameters




### -param lpszLibName [in]

The name of the library to be loaded.


### -param bAutoFree [in]

This parameter is maintained for compatibility with 16-bit applications, but is ignored.


## -returns



If the function succeeds, the return value is a handle to the loaded library; otherwise, it is <b>NULL</b>.




## -remarks



The <a href="https://msdn.microsoft.com/65e758ce-50a4-49e8-b3b2-0cd148d2781a">CoGetClassObject</a> function does not call <b>CoLoadLibrary</b>. <b>CoLoadLibrary</b> loads a DLL specified by the <i>lpszLibName</i> parameter into the process that called <b>CoGetClassObject</b>. Containers should not call <b>CoLoadLibrary</b> directly.

Internally, a reference count is kept on the loaded DLL by using <b>CoLoadLibrary</b> to increment the count and the <a href="https://msdn.microsoft.com/3959e7d9-6220-474e-8f85-76f7f935727f">CoFreeLibrary</a> function to decrement it.





## -see-also




<a href="https://msdn.microsoft.com/20616c05-21c6-4895-a1b5-4bae1aa417c7">CoFreeAllLibraries</a>



<a href="https://msdn.microsoft.com/3959e7d9-6220-474e-8f85-76f7f935727f">CoFreeLibrary</a>



<a href="https://msdn.microsoft.com/188e9a3b-39cc-454e-af65-4ac797e275d4">CoFreeUnusedLibraries</a>



<a href="https://msdn.microsoft.com/01660e9d-d8f2-40ef-a6d6-b80f0140ab5f">CoFreeUnusedLibrariesEx</a>
 

 

