---
UID: NF:shlobj.SHOpenPropSheetA
title: SHOpenPropSheetA function (shlobj.h)
description: SHOpenPropSheet may be altered or unavailable. (ANSI)
helpviewer_keywords: ["SHOpenPropSheetA", "shlobj/SHOpenPropSheetA"]
old-location: shell\SHOpenPropSheetW.htm
tech.root: shell
ms.assetid: bf42b26e-0f10-47b4-9d3b-48c59618342d
ms.date: 12/05/2018
ms.keywords: SHOpenPropSheet, SHOpenPropSheet function [Windows Shell], SHOpenPropSheetA, SHOpenPropSheetW, _win32_SHOpenPropSheetW, shell.SHOpenPropSheetW, shlobj/SHOpenPropSheet, shlobj/SHOpenPropSheetA, shlobj/SHOpenPropSheetW
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHOpenPropSheetW (Unicode) and SHOpenPropSheetA (ANSI)
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
 - SHOpenPropSheetA
 - shlobj/SHOpenPropSheetA
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
 - SHOpenPropSheet
 - SHOpenPropSheetA
 - SHOpenPropSheetW
---

# SHOpenPropSheetA function


## -description

<p class="CCE_Message">[<b>SHOpenPropSheet</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates a property sheet from a list of registry keys that contain the <b>CLSID</b>s of the individual sheets, then opens the property sheet.

## -parameters

### -param pszCaption [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a string that contains the caption for the property sheet. This value can be <b>NULL</b> if no caption is needed.

### -param ahkeys [in, optional]

Type: <b>HKEY[]</b>

An array of registry keys that represent the <b>CLSID</b>s of the individual property sheets.

### -param ckeys

Type: <b>UINT</b>

<b>UINT</b> value that specifies the number of property sheets in the array specified by <i>ahkeys</i>.

### -param pclsidDefault [in, optional]

Type: <b>const CLSID*</b>

A pointer to the default <b>CLSID</b>. This value can be <b>NULL</b>.

### -param pdtobj [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>*</b>

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>, an OLE object that can be used to carry out actions on the property sheet(s).

### -param psb [in, optional]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a>*</b>

Not used.

### -param pStartPage [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a string that specifies the start page. This value can be <b>NULL</b>.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if the property sheet was successfully created; otherwise, <b>FALSE</b>.

## -remarks

> [!NOTE]
> The shlobj.h header defines SHOpenPropSheet as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
