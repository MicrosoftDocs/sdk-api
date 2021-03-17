---
UID: NF:shlobj.PathProcessCommand
title: PathProcessCommand function (shlobj.h)
description: Deprecated. Processes a string that contains a command line and generates a suitably quoted string, with arguments attached if required.
helpviewer_keywords: ["PPCF_ADDARGUMENTS","PPCF_ADDQUOTES","PPCF_FORCEQUALIFY","PPCF_LONGESTPOSSIBLE","PPCF_NODIRECTORIES","PathProcessCommand","PathProcessCommand function [Windows Shell]","_win32_PathProcessCommand","shell.PathProcessCommand","shlobj/PathProcessCommand"]
old-location: shell\PathProcessCommand.htm
tech.root: shell
ms.assetid: 9dbc39e7-f73b-450f-bb87-17a38e7ab66d
ms.date: 12/05/2018
ms.keywords: PPCF_ADDARGUMENTS, PPCF_ADDQUOTES, PPCF_FORCEQUALIFY, PPCF_LONGESTPOSSIBLE, PPCF_NODIRECTORIES, PathProcessCommand, PathProcessCommand function [Windows Shell], _win32_PathProcessCommand, shell.PathProcessCommand, shlobj/PathProcessCommand
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PathProcessCommand
 - shlobj/PathProcessCommand
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - PathProcessCommand
---

# PathProcessCommand function


## -description

Deprecated. Processes a string that contains a command line and generates a suitably quoted string, with arguments attached if required.

## -parameters

### -param pszSrc [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated string that contains the command line to process.

### -param pszDest [out]

Type: <b>PWSTR</b>

Pointer to a buffer that receives a null-terminated Unicode string with the appropriate quotation marks. To determine how large this buffer must be, set this parameter to <b>NULL</b>. The function returns the required buffer size.

### -param cchDest

Type: <b>int</b>

The maximum number of characters that can be put in <i>pszDest</i>, not including the terminating null character. If this value is too small, the function fails.

### -param dwFlags

Type: <b>DWORD</b>

Flags that control the procedure. One or more of the following values:



#### PPCF_ADDQUOTES (0x00000001)

Add quotes if the path requires them.



#### PPCF_ADDARGUMENTS (0x00000003)

Append trailing arguments to the output string. This value includes <b>PPCF_ADDQUOTES</b>.



#### PPCF_NODIRECTORIES (0x00000010)

Do not match the input string against folders, only against file objects.



#### PPCF_FORCEQUALIFY (0x00000040)

Qualify even non-relative file names.



#### PPCF_LONGESTPOSSIBLE (0x00000080)

Always choose the longest possible executable name.

## -returns

Type: <b>LONG</b>

Returns a positive value if successful. If <i>lpDest</i> is set to <b>NULL</b>, the function returns the required buffer size in characters, including the terminating null character. If the call fails, the function returns a negative value.

## -remarks

<div class="alert"><b>Note</b>  This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It is not supported in Windows Vista and later versions of Windows.</div>
<div> </div>

