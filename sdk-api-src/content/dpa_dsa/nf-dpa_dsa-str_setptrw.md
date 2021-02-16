---
UID: NF:dpa_dsa.Str_SetPtrW
title: Str_SetPtrW function (dpa_dsa.h)
description: Sets ppszCurrent to a copy of pszNew and frees the previous value, if necessary.
helpviewer_keywords: ["Str_SetPtr","Str_SetPtr function [Windows Controls]","Str_SetPtrA","Str_SetPtrW","_win32_Str_SetPtrW","_win32_Str_SetPtrW_cpp","controls.Str_SetPtrW","controls._win32_Str_SetPtrW","dpa_dsa/Str_SetPtr","dpa_dsa/Str_SetPtrA","dpa_dsa/Str_SetPtrW"]
old-location: controls\Str_SetPtrW.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\str_setptrw.htm
ms.date: 12/05/2018
ms.keywords: Str_SetPtr, Str_SetPtr function [Windows Controls], Str_SetPtrA, Str_SetPtrW, _win32_Str_SetPtrW, _win32_Str_SetPtrW_cpp, controls.Str_SetPtrW, controls._win32_Str_SetPtrW, dpa_dsa/Str_SetPtr, dpa_dsa/Str_SetPtrA, dpa_dsa/Str_SetPtrW
req.header: dpa_dsa.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: Str_SetPtrW (Unicode) and Str_SetPtrA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comctl32.lib
req.dll: ComCtl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Str_SetPtrW
 - dpa_dsa/Str_SetPtrW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComCtl32.dll
api_name:
 - Str_SetPtr
 - Str_SetPtrA
 - Str_SetPtrW
---

# Str_SetPtrW function


## -description

Sets <i>ppszCurrent</i> to a copy of <i>pszNew</i> and frees the previous value, if necessary.

## -parameters

### -param ppsz [in, out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a>*</b>

The address of a pointer to the current string. The current string is freed and the pointer is set to a copy of <i>pszNew</i>.

### -param psz

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

A pointer to the string to copy into <i>ppszCurrent</i>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns <b>TRUE</b> if successful; otherwise, <b>FALSE</b>.

## -remarks

The ANSI version of <b>Str_SetPtrW</b>, <b>Str_SetPtrA</b>, is not exported by name or declared in a public header file. To use it, you must use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> and request ordinal 234 from ComCtl32.dll to obtain a function pointer.