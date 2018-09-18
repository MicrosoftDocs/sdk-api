---
UID: NF:shlobj_core.SHDestroyPropSheetExtArray
title: SHDestroyPropSheetExtArray function
author: windows-sdk-content
description: Frees property sheet handlers that are pointed to an array created by SHCreatePropSheetExtArray.
old-location: shell\SHDestroyPropSheetExtArray.htm
tech.root: shell
ms.assetid: beb3c1b1-deef-440d-8cf7-f76b3f396efa
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: SHDestroyPropSheetExtArray, SHDestroyPropSheetExtArray function [Windows Shell], _win32_SHDestroyPropSheetExtArray, shell.SHDestroyPropSheetExtArray, shlobj_core/SHDestroyPropSheetExtArray
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHDestroyPropSheetExtArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHDestroyPropSheetExtArray function


## -description


<p class="CCE_Message">[<b>SHDestroyPropSheetExtArray</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Frees property sheet handlers that are pointed to an array created by <a href="https://msdn.microsoft.com/88a72529-325d-431e-bc26-bddca787e62b">SHCreatePropSheetExtArray</a>.


## -parameters




### -param hpsxa [in]

Type: <b>HPSXA</b>

The handle of the array that contains pointers to the property sheet handlers to destroy.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/e0570cd6-dda2-43e4-8540-58baef37bf18">SHAddFromPropSheetExtArray</a>



<a href="https://msdn.microsoft.com/88a72529-325d-431e-bc26-bddca787e62b">SHCreatePropSheetExtArray</a>



<a href="https://msdn.microsoft.com/a8bdde44-d668-46c4-9e58-7a45b775fe09">SHReplaceFromPropSheetExtArray</a>
 

 

