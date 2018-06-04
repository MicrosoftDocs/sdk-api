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

# Str_SetPtrW function


## -description


Sets <i>ppszCurrent</i> to a copy of <i>pszNew</i> and frees the previous value, if necessary.


## -parameters




### -param ppsz

TBD


### -param psz

TBD




#### - ppszCurrent [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a>*</b>

The address of a pointer to the current string. The current string is freed and the pointer is set to a copy of <i>pszNew</i>.


#### - pszNew

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

A pointer to the string to copy into <i>ppszCurrent</i>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns <b>TRUE</b> if successful; otherwise, <b>FALSE</b>.




## -remarks



The ANSI version of <b>Str_SetPtrW</b>, <b>Str_SetPtrA</b>, is not exported by name or declared in a public header file. To use it, you must use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> and request ordinal 234 from ComCtl32.dll to obtain a function pointer.



