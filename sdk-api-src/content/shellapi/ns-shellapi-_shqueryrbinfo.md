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

# _SHQUERYRBINFO structure


## -description


Contains the size and item count information retrieved by the <a href="https://msdn.microsoft.com/a9a80486-2c99-4916-af25-10b00573456b">SHQueryRecycleBin</a> function.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of the structure, in bytes. This member must be filled in prior to calling the function.


### -field i64Size

Type: <b>__int64</b>

The total size of all the objects in the specified Recycle Bin, in bytes.


### -field i64NumItems

Type: <b>__int64</b>

The total number of items in the specified Recycle Bin.

