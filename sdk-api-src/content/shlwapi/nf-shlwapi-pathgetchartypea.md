---
UID: NF:shlwapi.PathGetCharTypeA
title: PathGetCharTypeA function (shlwapi.h)
author: windows-sdk-content
description: Determines the type of character in relation to a path.
old-location: shell\PathGetCharType.htm
tech.root: shell
ms.assetid: 838a255f-413e-424c-819e-47265224208d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PathGetCharType, PathGetCharType function [Windows Shell], PathGetCharTypeA, PathGetCharTypeW, _win32_PathGetCharType, shell.PathGetCharType, shlwapi/PathGetCharType, shlwapi/PathGetCharTypeA, shlwapi/PathGetCharTypeW
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathGetCharTypeW (Unicode) and PathGetCharTypeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-shlwapi-legacy-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - PathGetCharType
 - PathGetCharTypeA
 - PathGetCharTypeW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathGetCharTypeA function


## -description


Determines the type of character in relation to a path.


## -parameters




### -param ch [in]

Type: <b>TUCHAR</b>

The character for which to determine the type.


## -returns



Type: <b>UINT</b>

Returns one or more of the following values that define the type of character.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GCT_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The character is not valid in a path.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GCT_LFNCHAR</b></dt>
</dl>
</td>
<td width="60%">
The character is valid in a long file name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GCT_SEPARATOR</b></dt>
</dl>
</td>
<td width="60%">
The character is a path separator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GCT_SHORTCHAR</b></dt>
</dl>
</td>
<td width="60%">
The character is valid in a short (8.3) file name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GCT_WILD</b></dt>
</dl>
</td>
<td width="60%">
The character is a wildcard character.

</td>
</tr>
</table>
 



