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

# PathFindOnPathA function


## -description


Searches for a file.


## -parameters




### -param pszPath

TBD


### -param ppszOtherDirs [in, optional]

Type: <b>LPCTSTR*</b>

An optional, null-terminated array of directories to be searched first. This value can be <b>NULL</b>.


#### - pszFile [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the file name for which to search. If the search is successful, this parameter is used to return the fully qualified path name.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -remarks



<b>PathFindOnPath</b> searches for the file specified by <i>pszFile</i>. If no directories are specified in <i>ppszOtherDirs</i>, it attempts to find the file by searching standard directories such as System32 and the directories specified in the PATH environment variable. To expedite the process or enable <b>PathFindOnPath</b> to search a wider range of directories, use the <i>ppszOtherDirs</i> parameter to specify one or more directories to be searched first. If more than one file has the name specified by <i>pszFile</i>, <b>PathFindOnPath</b> returns the first instance it finds.



