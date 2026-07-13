---
UID: NF:shellapi.ExtractAssociatedIconExW
title: ExtractAssociatedIconExW function (shellapi.h)
description: ExtractAssociatedIconEx may be altered or unavailable. (Unicode)
helpviewer_keywords: ["ExtractAssociatedIconEx", "ExtractAssociatedIconEx function [Windows Shell]", "ExtractAssociatedIconExW", "_win32_ExtractAssociatedIconEx", "shell.ExtractAssociatedIconEx", "shellapi/ExtractAssociatedIconEx", "shellapi/ExtractAssociatedIconExW"]
old-location: shell\ExtractAssociatedIconEx.htm
tech.root: shell
ms.assetid: f32260b0-917b-4406-aeee-34f71a7c7309
ms.date: 12/05/2018
ms.keywords: ExtractAssociatedIconEx, ExtractAssociatedIconEx function [Windows Shell], ExtractAssociatedIconExA, ExtractAssociatedIconExW, _win32_ExtractAssociatedIconEx, shell.ExtractAssociatedIconEx, shellapi/ExtractAssociatedIconEx, shellapi/ExtractAssociatedIconExA, shellapi/ExtractAssociatedIconExW
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ExtractAssociatedIconExW (Unicode) and ExtractAssociatedIconExA (ANSI)
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
 - ExtractAssociatedIconExW
 - shellapi/ExtractAssociatedIconExW
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
 - ExtractAssociatedIconEx
 - ExtractAssociatedIconExA
 - ExtractAssociatedIconExW
---

# ExtractAssociatedIconExW function


## -description

<p class="CCE_Message">[<b>ExtractAssociatedIconEx</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets a handle to an icon stored as a resource in a file or an icon stored in a file's associated executable file. It extends the <a href="/windows/desktop/api/shellapi/nf-shellapi-extractassociatedicona">ExtractAssociatedIcon</a> function by retrieving the icon's ID when that icon is extracted from an executable file.

## -parameters

### -param hInst [in]

Type: <b>HINSTANCE</b>

The handle of the module from which to extract the icon.

### -param pszIconPath [in, out]

Type: <b>LPTSTR</b>

Pointer to a string that, on entry, specifies the full path and file name of the file that contains the icon. The function extracts the icon handle from that file, or from an executable file associated with that file. 

                    

When this function returns, if the icon handle was obtained from an executable file (either an executable file directly pointed to by this parameter or an associated executable file) the function stores the full path and file name of that executable in the buffer pointed to by this parameter.

### -param piIconIndex [in, out]

Type: <b>LPWORD</b>

Pointer to a <b>WORD</b> value that, on entry, specifies the index of the icon whose handle is to be obtained. 

                    

When the function returns, if the icon handle was obtained from an executable file (either an executable file pointed to by <i>lpIconPath</i> or an associated executable file), this value points to the icon's index in that file.

### -param piIconId [in, out]

Type: <b>LPWORD</b>

Pointer to a <b>WORD</b> value that, on entry, specifies the ID of the icon whose handle is to be obtained.

                    

When the function returns, if the icon handle was obtained from an executable file (either an executable file pointed to by <i>lpIconPath</i> or an associated executable file), this value points to the icon's ID within that file.

## -returns

Type: <b>HICON</b>

Returns the icon's handle if successful, otherwise <b>NULL</b>.

## -remarks

The icon handle returned by this function must be released by calling <a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a> when it is no longer needed.





> [!NOTE]
> The shellapi.h header defines ExtractAssociatedIconEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shellapi/nf-shellapi-extractassociatedicona">ExtractAssociatedIcon</a>



<a href="/windows/desktop/api/shellapi/nf-shellapi-extracticona">ExtractIcon</a>



<a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa">ExtractIconEx</a>
