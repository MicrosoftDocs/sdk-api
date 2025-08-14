---
UID: NF:shellapi.ExtractAssociatedIconW
title: ExtractAssociatedIconW function (shellapi.h)
description: Gets a handle to an icon stored as a resource in a file or an icon stored in a file's associated executable file. (Unicode)
helpviewer_keywords: ["ExtractAssociatedIcon", "ExtractAssociatedIcon function [Windows Shell]", "ExtractAssociatedIconW", "_shell_ExtractAssociatedIcon", "shell.ExtractAssociatedIcon", "shellapi/ExtractAssociatedIcon", "shellapi/ExtractAssociatedIconW"]
old-location: shell\ExtractAssociatedIcon.htm
tech.root: shell
ms.assetid: 157ce603-9988-4cae-a2cd-51db290268c3
ms.date: 12/05/2018
ms.keywords: ExtractAssociatedIcon, ExtractAssociatedIcon function [Windows Shell], ExtractAssociatedIconA, ExtractAssociatedIconW, _shell_ExtractAssociatedIcon, shell.ExtractAssociatedIcon, shellapi/ExtractAssociatedIcon, shellapi/ExtractAssociatedIconA, shellapi/ExtractAssociatedIconW
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ExtractAssociatedIconW (Unicode) and ExtractAssociatedIconA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ExtractAssociatedIconW
 - shellapi/ExtractAssociatedIconW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-5-0.dll
 - ext-ms-win-shell-shell32-l1-4-0.dll
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - Shell32.dll
 - Ext-MS-Win-Shell-Shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - ExtractAssociatedIcon
 - ExtractAssociatedIconA
 - ExtractAssociatedIconW
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# ExtractAssociatedIconW function


## -description

Gets a handle to an icon stored as a resource in a file or an icon stored in a file's associated executable file.

## -parameters

### -param hInst [in]

Type: <b>HINSTANCE</b>

A handle to the instance of the calling application.

### -param pszIconPath [in, out]

Type: <b>LPTSTR</b>

Pointer to a string that, on entry, specifies the full path and file name of the file that contains the icon. The function extracts the icon handle from that file, or from an executable file associated with that file. 

                    

When this function returns, if the icon handle was obtained from an executable file (either an executable file pointed to by <i>lpIconPath</i> or an associated executable file) the function stores the full path and file name of that executable in the buffer pointed to by this parameter.

### -param piIcon [in, out]

Type: <b>LPWORD</b>

Pointer to a <b>WORD</b> value that, on entry, specifies the index of the icon whose handle is to be obtained. 

                    

When the function returns, if the icon handle was obtained from an executable file (either an executable file pointed to by <i>lpIconPath</i> or an associated executable file), this value points to the icon's index in that file.

## -returns

Type: <b>HICON</b>

If the function succeeds, the return value is an icon handle. If the icon is extracted from an associated executable file, the function stores the full path and file name of the executable file in the string pointed to by <i>lpIconPath</i>, and stores the icon's identifier in the <b>WORD</b> pointed to by <i>lpiIcon</i>.

					

If the function fails, the return value is <b>NULL</b>.

## -remarks

When it is no longer needed, the caller is responsible for freeing the icon handle returned by <b>ExtractAssociatedIcon</b> by calling the <a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a> function.

The <b>ExtractAssociatedIcon</b> function first looks for the indexed icon in the file specified by <i>lpIconPath</i>. If the function cannot obtain the icon handle from that file, and the file has an associated executable file, it looks in that executable file for an icon. Associations with executable files are based on file name extensions and are stored in the per-user part of the registry.





> [!NOTE]
> The shellapi.h header defines ExtractAssociatedIcon as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shellapi/nf-shellapi-extractassociatediconexa">ExtractAssociatedIconEx</a>



<a href="/windows/desktop/api/shellapi/nf-shellapi-extracticona">ExtractIcon</a>



<a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa">ExtractIconEx</a>
