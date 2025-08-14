---
UID: NF:shlobj_core.ILCreateFromPathW
title: ILCreateFromPathW function (shlobj_core.h)
description: The ILCreateFromPathW (Unicode) function returns the ITEMIDLIST structure associated with a specified file path.
helpviewer_keywords: ["ILCreateFromPath", "ILCreateFromPath function [Windows Shell]", "ILCreateFromPathW", "_win32_ILCreateFromPathW", "shell.ILCreateFromPathW", "shlobj_core/ILCreateFromPath", "shlobj_core/ILCreateFromPathW"]
old-location: shell\ILCreateFromPathW.htm
tech.root: shell
ms.assetid: dee5486c-8be9-46c1-b5a1-e917e7c1e528
ms.date: 08/02/2022
ms.keywords: ILCreateFromPath, ILCreateFromPath function [Windows Shell], ILCreateFromPathA, ILCreateFromPathW, _win32_ILCreateFromPathW, shell.ILCreateFromPathW, shlobj_core/ILCreateFromPath, shlobj_core/ILCreateFromPathA, shlobj_core/ILCreateFromPathW
req.header: shlobj_core.h
req.include-header: Shlobj.h, Shlobj_core.h, Shlobj.h, Shlobj_core.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ILCreateFromPathW (Unicode) and ILCreateFromPathA (ANSI)
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
 - ILCreateFromPathW
 - shlobj_core/ILCreateFromPathW
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
 - ILCreateFromPath
 - ILCreateFromPathA
 - ILCreateFromPathW
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# ILCreateFromPathW function


## -description

Returns the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure associated with a specified file path.

## -parameters

### -param pszPath [in]

Type: <b>PCTSTR</b>

A pointer to a null-terminated Unicode string that contains the path. This string should be no more than MAX_PATH characters in length, including the terminating null character.

## -returns

Type: <b>PIDLIST_ABSOLUTE</b>

Returns a pointer to an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure that corresponds to the path.

## -remarks

Call <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree">ILFree</a> to release the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> when you are finished with it.




> [!NOTE]
> The shlobj_core.h header defines ILCreateFromPath as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
