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

# SHRegGetIntW function


## -description


Reads a numeric string value from the registry and converts it to an integer.


## -parameters




### -param hk [in]

Type: <b>HKEY</b>

A handle to the registry key that specifies the value to be read.


### -param pwzKey

TBD


### -param iDefault

TBD




#### - nDefault [in]

Type: <b>int</b>

An <b>int</b> that specifies the value returned if the registry value cannot be retrieved successfully.


#### - szKey [in]

Type: <b>LPCWSTR</b>

A pointer to a string value that specifies the name of the value to be read. The string must be null-terminated.


## -returns



Type: <b>int</b>

Returns the converted string as an <b>int</b>, or the default value specified by <i>nDefault</i>.




## -remarks



Prior to Windows 2000 Service Pack 3 (SP3), Windows Server 2003 Service Pack 1 (SP1), and Windows XP, <b>SHRegGetIntW</b> was not exported by name. On those systems you must load it directly from Shlwapi.dll as ordinal 280.

This function is only available in a Unicode version. ANSI is not supported.



