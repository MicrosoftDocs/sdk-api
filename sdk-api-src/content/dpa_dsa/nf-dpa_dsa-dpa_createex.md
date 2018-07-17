---
UID: NF:dpa_dsa.DPA_CreateEx
title: DPA_CreateEx function
author: windows-sdk-content
description: Creates a dynamic pointer array (DPA) using a given specified size and heap location.
old-location: controls\DPA_CreateEx.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_createex.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: DPA_CreateEx, DPA_CreateEx function [Windows Controls], _shell_DPA_CreateEx, _shell_DPA_CreateEx_cpp, controls.DPA_CreateEx, controls._shell_DPA_CreateEx, dpa_dsa/DPA_CreateEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dpa_dsa.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
tech.root: 
req.typenames: CRYPTPROTECT_PROMPTSTRUCT, *PCRYPTPROTECT_PROMPTSTRUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComCtl32.dll
api_name:
 - DPA_CreateEx
product: Windows
targetos: Windows
req.lib: 
req.dll: ComCtl32.dll (version 4.0 or later)
req.irql: 
---

# DPA_CreateEx function


## -description


Creates a dynamic pointer array (DPA) using a given specified size and heap location.


## -parameters




### -param cpGrow [in]

Type: <b>int</b>

The number of elements by which the array should be expanded, if the DPA needs to be enlarged.


### -param hheap [in, optional]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/hh973215">HANDLE</a></b>

A handle to the heap where the array is stored.


## -returns



Type: <b>HDPA</b>

Returns a handle to a DPA if successful, or <b>NULL</b> if the call fails.




## -remarks



<b>DPA_CreateEx</b> is not exported by name. To use it, you must use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> and request ordinal 340 from ComCtl32.dll to obtain a function pointer.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb775603(v=VS.85).aspx">DPA_Create</a>
 

 

