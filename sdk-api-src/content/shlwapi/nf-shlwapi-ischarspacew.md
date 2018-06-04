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

# IsCharSpaceW function


## -description


Determines whether a character represents a space.


## -parameters




### -param wch [in]

Type: <b>TCHAR</b>

A single character.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the character is a space; otherwise, <b>FALSE</b>.




## -remarks



For those versions of Windows that do not include <b>IsCharSpace</b> in Shlwapi.h, <b>IsCharSpaceW</b> must be called directly from Shlwapi.dll (ordinal 29), using a WCHAR in the <i>wch</i> parameter. <b>IsCharSpaceA</b> is not available in versions of Windows that do not include <b>IsCharSpace</b> in Shlwapi.h.



