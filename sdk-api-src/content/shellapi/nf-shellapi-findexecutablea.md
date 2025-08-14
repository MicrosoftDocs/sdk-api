---
UID: NF:shellapi.FindExecutableA
title: FindExecutableA function (shellapi.h)
description: Retrieves the name of and handle to the executable (.exe) file associated with a specific document file. (ANSI)
helpviewer_keywords: ["FindExecutableA", "shellapi/FindExecutableA"]
old-location: shell\FindExecutable.htm
tech.root: shell
ms.assetid: 969edbd9-164e-457f-ab0a-dc4d069bf16b
ms.date: 12/05/2018
ms.keywords: FindExecutable, FindExecutable function [Windows Shell], FindExecutableA, FindExecutableW, _win32_FindExecutable, shell.FindExecutable, shellapi/FindExecutable, shellapi/FindExecutableA, shellapi/FindExecutableW
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindExecutableW (Unicode) and FindExecutableA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FindExecutableA
 - shellapi/FindExecutableA
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
 - FindExecutable
 - FindExecutableA
 - FindExecutableW
no-loc: [verb, verbs, NULL, null, runas]
---

# FindExecutableA function


## -description

Retrieves the name of and handle to the executable (.exe) file associated with a specific document file.

## -parameters

### -param lpFile [in]

Type: <b>LPCTSTR</b>

The address of a <b>null</b>-terminated string that specifies a file name. This file should be a document.

### -param lpDirectory [in, optional]

Type: <b>LPCTSTR</b>

The address of a <b>null</b>-terminated string that specifies the default directory. This value can be <b>NULL</b>.

### -param lpResult [out]

Type: <b>LPTSTR</b>

The address of a buffer that receives the file name of the associated executable file. This file name is a <b>null</b>-terminated string that specifies the executable file started when an ":::no-loc text="open":::" by association is run on the file specified in the <i>lpFile</i> parameter. Put simply, this is the application that is launched when the document file is directly double-clicked or when <b>Open</b> is chosen from the file's shortcut menu. This parameter must contain a valid non-<b>null</b> value and is assumed to be of length MAX_PATH. Responsibility for validating the value is left to the programmer.

## -returns

Type: <b>HINSTANCE</b>

Returns a value greater than 32 if successful, or a value less than or equal to 32 representing an error.
					
                    

The following table lists possible error values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SE_ERR_FNF</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The specified file was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SE_ERR_PNF</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The specified path is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SE_ERR_ACCESSDENIED</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The specified file cannot be accessed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SE_ERR_OOM</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The system is out of memory or resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SE_ERR_NOASSOC</b></dt>
<dt>31</dt>
</dl>
</td>
<td width="60%">
There is no association for the specified file type with an executable file.

</td>
</tr>
</table>

## -remarks

Use <b>FindExecutable</b> for documents. If you want to retrieve the path of an executable file, use the following:

				


```
AssocQueryString(ASSOCF_OPEN_BYEXENAME,
                 ASSOCSTR_EXECUTABLE,
                 pszExecutableName,
                 NULL,
                 pszPath,
                 pcchOut);
```


Here, <i>pszExecutableName</i> is a pointer to a <b>null</b>-terminated string that specifies the name of the executable file, <i>pszPath</i> is a pointer to the <b>null</b>-terminated string buffer that receives the path to the executable file, and <i>pcchOut</i> is a pointer to a <b>DWORD</b> that specifies the number of characters in the <i>pszPath</i> buffer. When the function returns, <i>pcchOut</i> is set to the number of characters actually placed in the buffer. See <a href="/windows/desktop/api/shlwapi/nf-shlwapi-assocquerystringa">AssocQueryString</a> for more information.

When <b>FindExecutable</b> returns, the <i>lpResult</i> parameter may contain the path to the Dynamic Data Exchange (DDE) server started if a server does not respond to a request to initiate a DDE conversation with the DDE client application.





> [!NOTE]
> The shellapi.h header defines FindExecutable as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecutea">ShellExecute</a>
