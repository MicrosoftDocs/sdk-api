---
UID: NS:shlobj_core._IDA
title: "_IDA"
author: windows-sdk-content
description: Used with the CFSTR_SHELLIDLIST clipboard format to transfer the pointer to an item identifier list (PIDL) of one or more Shell namespace objects.
old-location: shell\CIDA.htm
tech.root: shell
ms.assetid: 30caf91d-8f3c-48ea-ad64-47f919f33f1d
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: "*LPIDA, CIDA, CIDA structure [Windows Shell], LPIDA, LPIDA structure pointer [Windows Shell], _IDA, _win32_CIDA, shell.CIDA, shlobj_core/CIDA, shlobj_core/LPIDA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
 - shlobj_core.h
api_name:
 - CIDA
product: Windows
targetos: Windows
req.typenames: CIDA, *LPIDA
req.redist: 
---

# _IDA structure


## -description


Used with the <a href="https://msdn.microsoft.com/fb8ce5d3-3215-4e05-a916-4d4a803464d2">CFSTR_SHELLIDLIST</a> clipboard format to transfer the pointer to an item identifier list (PIDL) of one or more Shell namespace objects.


## -struct-fields




### -field cidl

Type: <b>UINT</b>

The number of PIDLs that are being transferred, not including the parent folder.


### -field aoffset

Type: <b>UINT[1]</b>

An array of offsets, relative to the beginning of this structure. The array contains <b>cidl</b>+1 elements. The first element of <b>aoffset</b> contains an offset to the fully qualified PIDL of a parent folder. If this PIDL is empty, the parent folder is the desktop. Each of the remaining elements of the array contains an offset to one of the PIDLs to be transferred. All of these PIDLs are relative to the PIDL of the parent folder.


## -remarks



To use this structure to retrieve a particular PIDL, add the <b>aoffset</b> value of the PIDL to the address of the structure. The following two macros can be used to retrieve PIDLs from the structure. The first retrieves the PIDL of the parent folder. The second retrieves a PIDL, specified by its zero-based index.
				
                


```
#define HIDA_GetPIDLFolder(pida) (LPCITEMIDLIST)(((LPBYTE)pida)+(pida)->aoffset[0])
#define HIDA_GetPIDLItem(pida, i) (LPCITEMIDLIST)(((LPBYTE)pida)+(pida)->aoffset[i+1])
```


The value that is returned by these macros is a pointer to the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure. Since these structures vary in length, you must determine the end of the structure by parsing it. See <a href="https://msdn.microsoft.com/c0d61bc6-6851-4b47-a62d-4c24d2958b98">NameSpace</a> for further discussion of PIDLs and the <b>ITEMIDLIST</b> structure.



