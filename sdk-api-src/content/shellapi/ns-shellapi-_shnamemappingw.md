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

# _SHNAMEMAPPINGW structure


## -description


Contains the old and new path names for each file that was moved, copied, or renamed by the <a href="https://msdn.microsoft.com/7807015f-52c5-46f5-9e90-4e3e60ddf705">SHFileOperation</a> function.


## -struct-fields




### -field pszOldPath

Type: <b>LPTSTR</b>

The address of a character buffer that contains the old path name.


### -field pszNewPath

Type: <b>LPTSTR</b>

The address of a character buffer that contains the new path name.


### -field cchOldPath

Type: <b>int</b>

The number of characters in <b>pszOldPath</b>.


### -field cchNewPath

Type: <b>int</b>

The number of characters in <b>pszNewPath</b>.


## -remarks



There are two versions of this structure, an ANSI version (SHFILEOPSTRUCTA) and a Unicode version (SHFILEOPSTRUCTW). The Unicode version is identical to the ANSI version, except that wide character strings (<b>LPCWSTR</b>) are used in place of ANSI character strings (<b>LPCSTR</b>). On Windows 98 and earlier, only the ANSI version is supported. On Microsoft Windows NT 4.0 and later, both the ANSI and Unicode versions of this structure are supported. SHNAMEMAPPINGA and SHNAMEMAPPINGW should never be used directly; the appropriate structure is redefined as <b>SHNAMEMAPPING</b> by the precompiler depending on whether the application is compiled for ANSI or Unicode.




## -see-also




<a href="https://msdn.microsoft.com/590d87c2-0c75-44b9-a9b5-f7c37728512b">SHFILEOPSTRUCT</a>
 

 

