---
UID: NS:shtypes._STRRET
title: "_STRRET"
author: windows-sdk-content
description: Contains strings returned from the IShellFolder interface methods.
old-location: shell\STRRET.htm
tech.root: shell
ms.assetid: 7868ef9b-07db-455b-b0be-ef0db7891447
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*LPSTRRET, LPSTRRET, LPSTRRET structure pointer [Windows Shell], STRRET, STRRET structure [Windows Shell], STRRET_CSTR, STRRET_OFFSET, STRRET_WSTR, _STRRET, _win32_STRRET, shell.STRRET, shtypes/LPSTRRET, shtypes/STRRET"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: shtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shtypes.h
api_name:
 - STRRET
product: Windows
targetos: Windows
req.typenames: STRRET
req.redist: 
---

# _STRRET structure


## -description


Contains strings returned from the <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> interface methods.


## -struct-fields




### -field uType

Type: <b>UINT</b>

A value that specifies the desired format of the string. This can be one of the following values.



#### STRRET_CSTR

The string is returned in the <b>cStr</b> member.



#### STRRET_OFFSET

The <b>uOffset</b> member value indicates the number of bytes from the beginning of the item identifier list where the string is located.



#### STRRET_WSTR

The string is at the address specified by <b>pOleStr</b> member.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.pOleStr

Type: <b>LPWSTR</b>

A pointer to the string. This memory must be allocated with <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>. It is the calling application's responsibility to free this memory with <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> when it is no longer needed.


### -field DUMMYUNIONNAME.uOffset

Type: <b>UINT</b>

The offset into the item identifier list.


### -field DUMMYUNIONNAME.cStr

Type: <b>CHAR[MAX_PATH]</b>

The buffer to receive the display name.


## -see-also




<a href="https://msdn.microsoft.com/2164bbe6-e030-4a64-85db-9ee1cd3c136d">IShellFolder::GetDisplayNameOf</a>
 

 

