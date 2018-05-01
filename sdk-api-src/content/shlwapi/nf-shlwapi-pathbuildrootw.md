---
UID: NF:shlwapi.PathBuildRootW
title: PathBuildRootW function
author: windows-driver-content
description: Creates a root path from a given drive number.
old-location: shell\PathBuildRoot.htm
old-project: shell
ms.assetid: 0a6895bd-54cf-499c-9057-f2d721bce5d9
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: PathBuildRoot, PathBuildRoot function [Windows Shell], PathBuildRootA, PathBuildRootW, _win32_PathBuildRoot, shell.PathBuildRoot, shlwapi/PathBuildRoot, shlwapi/PathBuildRootA, shlwapi/PathBuildRootW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathBuildRootW (Unicode) and PathBuildRootA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: URL_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shlwapi.dll
api_name:
-	PathBuildRoot
-	PathBuildRootA
-	PathBuildRootW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# PathBuildRootW function


## -description


Creates a root path from a given drive number.


## -parameters




### -param pszRoot

TBD


### -param iDrive [in]

Type: <b>int</b>

A variable of type <b>int</b> that indicates the desired drive number. It should be between 0 and 25.


#### - szRoot [out]

Type: <b>LPTSTR</b>

A pointer to the string that receives the constructed root path. This buffer must be at least four characters in size.


## -returns



Type: <b>LPTSTR</b>

Returns the address of the constructed root path. If the call fails for any reason (for example, an invalid drive number), <i>szRoot</i> is returned unchanged.



