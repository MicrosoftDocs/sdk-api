---
UID: NF:shellapi.SHQueryRecycleBinW
title: SHQueryRecycleBinW function (shellapi.h)
description: Retrieves the size of the Recycle Bin and the number of items in it, for a specified drive. (Unicode)
helpviewer_keywords: ["SHQueryRecycleBin", "SHQueryRecycleBin function [Windows Shell]", "SHQueryRecycleBinW", "_win32_SHQueryRecycleBin", "shell.SHQueryRecycleBin", "shellapi/SHQueryRecycleBin", "shellapi/SHQueryRecycleBinW"]
old-location: shell\SHQueryRecycleBin.htm
tech.root: shell
ms.assetid: a9a80486-2c99-4916-af25-10b00573456b
ms.date: 12/05/2018
ms.keywords: SHQueryRecycleBin, SHQueryRecycleBin function [Windows Shell], SHQueryRecycleBinA, SHQueryRecycleBinW, _win32_SHQueryRecycleBin, shell.SHQueryRecycleBin, shellapi/SHQueryRecycleBin, shellapi/SHQueryRecycleBinA, shellapi/SHQueryRecycleBinW
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHQueryRecycleBinW (Unicode) and SHQueryRecycleBinA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHQueryRecycleBinW
 - shellapi/SHQueryRecycleBinW
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
 - SHQueryRecycleBin
 - SHQueryRecycleBinA
 - SHQueryRecycleBinW
---

# SHQueryRecycleBinW function


## -description

Retrieves the size of the Recycle Bin and the number of items in it, for a specified drive.

## -parameters

### -param pszRootPath [in, optional]

Type: <b>LPCTSTR</b>

The address of a <b>null</b>-terminated string of maximum length MAX_PATH to contain the path of the root drive on which the Recycle Bin is located. This parameter can contain the address of a string formatted with the drive, folder, and subfolder names (C:\Windows\System...).

### -param pSHQueryRBInfo [in, out]

Type: <b>LPSHQUERYRBINFO</b>

The address of a <a href="/windows/desktop/api/shellapi/ns-shellapi-shqueryrbinfo">SHQUERYRBINFO</a> structure that receives the Recycle Bin information. The <b>cbSize</b> member of the structure must be set to the size of the structure before calling this API.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

With Windows 2000, if <b>NULL</b> is passed in the <i>pszRootPath</i> parameter, the function fails and returns an E_INVALIDARG error code. In earlier versions of the operating system, you can pass an empty string or <b>NULL</b>. If <i>pszRootPath</i> contains an empty string or <b>NULL</b>, information is retrieved for all Recycle Bins on all drives.





> [!NOTE]
> The shellapi.h header defines SHQueryRecycleBin as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shellapi/nf-shellapi-shemptyrecyclebina">SHEmptyRecycleBin</a>
