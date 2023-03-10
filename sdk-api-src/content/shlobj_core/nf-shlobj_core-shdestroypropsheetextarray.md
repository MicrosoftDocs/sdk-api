---
UID: NF:shlobj_core.SHDestroyPropSheetExtArray
title: SHDestroyPropSheetExtArray function (shlobj_core.h)
description: Frees property sheet handlers that are pointed to an array created by SHCreatePropSheetExtArray.
helpviewer_keywords: ["SHDestroyPropSheetExtArray","SHDestroyPropSheetExtArray function [Windows Shell]","_win32_SHDestroyPropSheetExtArray","shell.SHDestroyPropSheetExtArray","shlobj_core/SHDestroyPropSheetExtArray"]
old-location: shell\SHDestroyPropSheetExtArray.htm
tech.root: shell
ms.assetid: beb3c1b1-deef-440d-8cf7-f76b3f396efa
ms.date: 12/05/2018
ms.keywords: SHDestroyPropSheetExtArray, SHDestroyPropSheetExtArray function [Windows Shell], _win32_SHDestroyPropSheetExtArray, shell.SHDestroyPropSheetExtArray, shlobj_core/SHDestroyPropSheetExtArray
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - SHDestroyPropSheetExtArray
 - shlobj_core/SHDestroyPropSheetExtArray
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
 - SHDestroyPropSheetExtArray
---

# SHDestroyPropSheetExtArray function


## -description

<p class="CCE_Message">[<b>SHDestroyPropSheetExtArray</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Frees property sheet handlers that are pointed to an array created by <a href="/windows/desktop/api/shlobj/nf-shlobj-shcreatepropsheetextarray">SHCreatePropSheetExtArray</a>.

## -parameters

### -param hpsxa [in]

Type: <b>HPSXA</b>

The handle of the array that contains pointers to the property sheet handlers to destroy.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddfrompropsheetextarray">SHAddFromPropSheetExtArray</a>



<a href="/windows/desktop/api/shlobj/nf-shlobj-shcreatepropsheetextarray">SHCreatePropSheetExtArray</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shreplacefrompropsheetextarray">SHReplaceFromPropSheetExtArray</a>