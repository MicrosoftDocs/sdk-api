---
UID: NS:shellapi._SHNAMEMAPPINGA
title: SHNAMEMAPPINGA (shellapi.h)
author: windows-sdk-content
description: Contains the old and new path names for each file that was moved, copied, or renamed by the SHFileOperation function.
old-location: shell\SHNAMEMAPPING.htm
tech.root: shell
ms.assetid: c77f5ed6-3c7f-48dd-8bb6-33d6d3053238
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*LPSHNAMEMAPPINGA, LPSHNAMEMAPPING, LPSHNAMEMAPPING structure pointer [Windows Shell], SHNAMEMAPPING, SHNAMEMAPPING structure [Windows Shell], SHNAMEMAPPINGA, _win32_SHNAMEMAPPING, shell.SHNAMEMAPPING, shellapi/LPSHNAMEMAPPING, shellapi/SHNAMEMAPPING'
ms.topic: struct
f1_keywords:
- shellapi/SHNAMEMAPPING
dev_langs:
 - c++
req.header: shellapi.h
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
- Shellapi.h
api_name:
- SHNAMEMAPPING
 - SHNAMEMAPPINGA
targetos: Windows
req.typenames: SHNAMEMAPPINGA, *LPSHNAMEMAPPINGA
req.redist: 
ms.custom: 19H1
---

# SHNAMEMAPPINGA structure


## -description


Contains the old and new path names for each file that was moved, copied, or renamed by the <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a> function.


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




<a href="https://docs.microsoft.com/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa">SHFILEOPSTRUCT</a>
 

 

