---
UID: NF:shellapi.ExtractIconW
title: ExtractIconW function (shellapi.h)
description: Gets a handle to an icon from the specified executable file, DLL, or icon file. To retrieve an array of handles to large or small icons, use the ExtractIconEx function. (Unicode)
helpviewer_keywords: ["ExtractIcon", "ExtractIcon function [Windows Shell]", "ExtractIconW", "_shell_ExtractIcon", "shell.ExtractIcon", "shellapi/ExtractIcon", "shellapi/ExtractIconW"]
old-location: shell\ExtractIcon.htm
tech.root: shell
ms.assetid: a0314423-79d6-416e-8be0-be946477da3e
ms.date: 12/05/2018
ms.keywords: ExtractIcon, ExtractIcon function [Windows Shell], ExtractIconA, ExtractIconW, _shell_ExtractIcon, shell.ExtractIcon, shellapi/ExtractIcon, shellapi/ExtractIconA, shellapi/ExtractIconW
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ExtractIconW (Unicode) and ExtractIconA (ANSI)
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
 - ExtractIconW
 - shellapi/ExtractIconW
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
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - ExtractIcon
 - ExtractIconA
 - ExtractIconW
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# ExtractIconW function


## -description

Gets a handle to an icon from the specified executable file, DLL, or icon file.

            

To retrieve an array of handles to large or small icons, use the <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa">ExtractIconEx</a> function.

## -parameters

### -param hInst [in]

Type: <b>HINSTANCE</b>

Handle to the instance of the application that calls the function.

### -param pszExeFileName [in]

Type: <b>LPCTSTR</b>

Pointer to a null-terminated string that specifies the name of an executable file, DLL, or icon file.

### -param nIconIndex

Type: <b>UINT</b>

Specifies the zero-based index of the icon to retrieve. For example, if this value is 0, the function returns a handle to the first icon in the specified file. 
                    
                    

If this value is -1, the function returns the total number of icons in the specified file. If the file is an executable file or DLL, the return value is the number of RT_GROUP_ICON resources. If the file is an .ICO file, the return value is 1.

If this value is a negative number not equal to –1, the function returns a handle to the icon in the specified file whose resource identifier is equal to the absolute value of <i>nIconIndex</i>. For example, you should use –3 to extract the icon whose resource identifier is 3. To extract the icon whose resource identifier is 1, use the <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa">ExtractIconEx</a> function.

## -returns

Type: <b>HICON</b>

The return value is a handle to an icon. If the file specified was not an executable file, DLL, or icon file, the return is 1. If no icons were found in the file, the return value is <b>NULL</b>.

## -remarks

When it is no longer needed, you must destroy the icon handle returned by <b>ExtractIcon</b> by calling the <a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a> function.





> [!NOTE]
> The shellapi.h header defines ExtractIcon as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shellapi/nf-shellapi-extractassociatedicona">ExtractAssociatedIcon</a>



<a href="/windows/desktop/api/shellapi/nf-shellapi-extractassociatediconexa">ExtractAssociatedIconEx</a>



<a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa">ExtractIconEx</a>
