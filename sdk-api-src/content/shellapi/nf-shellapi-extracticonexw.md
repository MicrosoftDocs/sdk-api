---
UID: NF:shellapi.ExtractIconExW
title: ExtractIconExW function (shellapi.h)
description: The ExtractIconEx function creates an array of handles to large or small icons extracted from the specified executable file, DLL, or icon file. (Unicode)
helpviewer_keywords: ["ExtractIconEx", "ExtractIconEx function [Windows Shell]", "ExtractIconExW", "_shell_ExtractIconEx", "shell.ExtractIconEx", "shellapi/ExtractIconEx", "shellapi/ExtractIconExW"]
old-location: shell\ExtractIconEx.htm
tech.root: shell
ms.assetid: 1c4d760a-79b5-4646-9cf2-6cd32c5d05ee
ms.date: 12/05/2018
ms.keywords: ExtractIconEx, ExtractIconEx function [Windows Shell], ExtractIconExA, ExtractIconExW, _shell_ExtractIconEx, shell.ExtractIconEx, shellapi/ExtractIconEx, shellapi/ExtractIconExA, shellapi/ExtractIconExW
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ExtractIconExW (Unicode) and ExtractIconExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: shell32.lib
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ExtractIconExW
 - shellapi/ExtractIconExW
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
 - ExtractIconEx
 - ExtractIconExA
 - ExtractIconExW
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# ExtractIconExW function


## -description

The <b>ExtractIconEx</b> function creates an array of handles to large or small icons extracted from the specified executable file, DLL, or icon file.

## -parameters

### -param lpszFile [in]

Type: <b>LPCTSTR</b>

Pointer to a null-terminated string that specifies the name of an executable file, DLL, or icon file from which icons will be extracted.

### -param nIconIndex [in]

Type: <b>int</b>

Specifies the zero-based index of the first icon to extract. For example, if this value is zero, the function extracts the first icon in the specified file. 
    
                        

If this value is –1 and <i>phiconLarge</i> and <i>phiconSmall</i> are both <b>NULL</b>, the function returns the total number of icons in the specified file. If the file is an executable file or DLL, the return value is the number of RT_GROUP_ICON resources. If the file is an .ico file, the return value is 1.

 If this value is a negative number and either <i>phiconLarge</i> or <i>phiconSmall</i> is not <b>NULL</b>, the function begins by extracting the icon whose resource identifier is equal to the absolute value of <i>nIconIndex</i>. For example, use -3 to extract the icon whose resource identifier is 3.

### -param phiconLarge [out]

Type: <b>HICON*</b>

Pointer to an array of icon handles that receives handles to the large icons extracted from the file. If this parameter is <b>NULL</b>, no large icons are extracted from the file.

### -param phiconSmall [out]

Type: <b>HICON*</b>

Pointer to an array of icon handles that receives handles to the small icons extracted from the file. If this parameter is <b>NULL</b>, no small icons are extracted from the file.

### -param nIcons

Type: <b>UINT</b>

The number of icons to extract from the file.

## -returns

Type: **UINT**

If the *nIconIndex* parameter is -1 and both the *phiconLarge* and *phiconSmall* parameters are **NULL**, then the return value is the number of icons contained in the specified file.

If the *nIconIndex* parameter is any value other than -1 and either *phiconLarge* or *phiconSmall* is not **NULL**, the return value is the number of icons successfully extracted from the file.

> [!NOTE]
> If the function encounters an error, it returns **UINT_MAX**. In this case, you can call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md) to retrieve the error code. For example, this function returns **UINT_MAX** if the file specified by *lpszFile* cannot be found while the *nIconIndex* parameter is any value other than -1 and either *phiconLarge* or *phiconSmall* is not **NULL**. In this case, **GetLastError** returns **ERROR_FILE_NOT_FOUND** (2).

## -remarks

When they are no longer needed, you must destroy all icons extracted by <b>ExtractIconEx</b> by calling the <a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a> function.

To retrieve the dimensions of the large and small icons, use this function with the SM_CXICON, SM_CYICON, SM_CXSMICON, and SM_CYSMICON flags.





> [!NOTE]
> The shellapi.h header defines ExtractIconEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shellapi/nf-shellapi-extractassociatedicona">ExtractAssociatedIcon</a>



<a href="/windows/desktop/api/shellapi/nf-shellapi-extractassociatediconexa">ExtractAssociatedIconEx</a>



<a href="/windows/desktop/api/shellapi/nf-shellapi-extracticona">ExtractIcon</a>
