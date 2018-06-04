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

# SHRegGetBoolUSValueA function


## -description


Retrieves a Boolean value from a registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).


## -parameters




### -param pszSubKey [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string with the name of the subkey relative to <b>HKEY_LOCAL_MACHINE</b> and <b>HKEY_CURRENT_USER</b>. For example, "Software\MyCompany\MyProduct".


### -param pszValue [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that specifies the name of the value. This value can be <b>NULL</b>.


### -param fIgnoreHKCU [in]

Type: <b>BOOL</b>

A variable that specifies which key to look under. When set to <b>TRUE</b>, <a href="https://msdn.microsoft.com/4d3b3bbe-dc2e-40c9-8ff1-0f9d2e323743">SHRegGetUSValue</a> ignores <b>HKEY_CURRENT_USER</b> and returns a value from <b>HKEY_LOCAL_MACHINE</b>.


### -param fDefault [in]

Type: <b>BOOL</b>

A value that is returned if there is no registry value.


## -returns



Type: <b>BOOL</b>

Returns either the value from the registry, or <i>fDefault</i> if none is found.



