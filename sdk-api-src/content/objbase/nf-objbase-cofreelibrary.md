---
UID: NF:objbase.CoFreeLibrary
title: CoFreeLibrary function
author: windows-driver-content
description: Frees a library that, when loaded, was specified to be freed explicitly.
old-location: com\cofreelibrary.htm
old-project: com
ms.assetid: 3959e7d9-6220-474e-8f85-76f7f935727f
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: CoFreeLibrary, CoFreeLibrary function [COM], _com_CoFreeLibrary, com.cofreelibrary, objbase/CoFreeLibrary
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
-	CoFreeLibrary
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CoFreeLibrary function


## -description


Frees a library that, when loaded, was specified to be freed explicitly.
<div class="alert"><b>Note</b>  This function is provided for compatibility with 16-bit Windows.</div><div> </div>

## -parameters




### -param hInst [in]

A handle to the library module to be freed, as returned by the <a href="https://msdn.microsoft.com/be0d9e82-2438-488e-88c3-68dc7ac3e16f">CoLoadLibrary</a> function.


## -returns



This function does not return a value.




## -remarks



The <b>CoFreeLibrary</b> function should be called to free a library that is to be freed explicitly. This is established when the library is loaded with the <i>bAutoFree</i> parameter of <a href="https://msdn.microsoft.com/be0d9e82-2438-488e-88c3-68dc7ac3e16f">CoLoadLibrary</a> set to <b>FALSE</b>. It is illegal to free a library explicitly when the corresponding <b>CoLoadLibrary</b> call specifies that it be freed automatically (the <i>bAutoFree</i> parameter is set to <b>TRUE</b>).






## -see-also




<a href="https://msdn.microsoft.com/20616c05-21c6-4895-a1b5-4bae1aa417c7">CoFreeAllLibraries</a>



<a href="https://msdn.microsoft.com/188e9a3b-39cc-454e-af65-4ac797e275d4">CoFreeUnusedLibraries</a>



<a href="https://msdn.microsoft.com/01660e9d-d8f2-40ef-a6d6-b80f0140ab5f">CoFreeUnusedLibrariesEx</a>



<a href="https://msdn.microsoft.com/be0d9e82-2438-488e-88c3-68dc7ac3e16f">CoLoadLibrary</a>
 

 

