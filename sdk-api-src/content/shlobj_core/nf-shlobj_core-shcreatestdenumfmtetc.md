---
UID: NF:shlobj_core.SHCreateStdEnumFmtEtc
title: SHCreateStdEnumFmtEtc function (shlobj_core.h)
description: SHCreateStdEnumFmtEtc may be altered or unavailable.
helpviewer_keywords: ["SHCreateStdEnumFmtEtc","SHCreateStdEnumFmtEtc function [Windows Shell]","_win32_SHCreateStdEnumFmtEtc","shell.SHCreateStdEnumFmtEtc","shlobj_core/SHCreateStdEnumFmtEtc"]
old-location: shell\SHCreateStdEnumFmtEtc.htm
tech.root: shell
ms.assetid: c391c8c8-6062-4e70-9a1f-de0eb610250d
ms.date: 12/05/2018
ms.keywords: SHCreateStdEnumFmtEtc, SHCreateStdEnumFmtEtc function [Windows Shell], _win32_SHCreateStdEnumFmtEtc, shell.SHCreateStdEnumFmtEtc, shlobj_core/SHCreateStdEnumFmtEtc
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
 - SHCreateStdEnumFmtEtc
 - shlobj_core/SHCreateStdEnumFmtEtc
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
 - windows.storage.dll
api_name:
 - SHCreateStdEnumFmtEtc
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# SHCreateStdEnumFmtEtc function


## -description

<p class="CCE_Message">[<b>SHCreateStdEnumFmtEtc</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates an <a href="/windows/desktop/api/objidl/nn-objidl-ienumformatetc">IEnumFORMATETC</a> object from an array of <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structures.

## -parameters

### -param cfmt [in]

Type: <b>UINT</b>

The number of entries in the <i>afmt</i> array.

### -param afmt

Type: <b>const <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a>[]</b>

An array of <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structures that specifies the clipboard formats of interest.

### -param ppenumFormatEtc [out]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ienumformatetc">IEnumFORMATETC</a>**</b>

When this function returns successfully, receives an <a href="/windows/desktop/api/objidl/nn-objidl-ienumformatetc">IEnumFORMATETC</a> interface pointer. Receives <b>NULL</b> on failure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
