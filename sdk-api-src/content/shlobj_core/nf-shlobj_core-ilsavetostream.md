---
UID: NF:shlobj_core.ILSaveToStream
title: ILSaveToStream function (shlobj_core.h)
description: Saves an ITEMIDLIST structure to a stream.
helpviewer_keywords: ["ILSaveToStream","ILSaveToStream function [Windows Shell]","_win32_ILSaveToStream","shell.ILSaveToStream","shlobj_core/ILSaveToStream"]
old-location: shell\ILSaveToStream.htm
tech.root: shell
ms.assetid: 40d5ce57-58dc-4c79-8fe6-5412e3d7dc64
ms.date: 12/05/2018
ms.keywords: ILSaveToStream, ILSaveToStream function [Windows Shell], _win32_ILSaveToStream, shell.ILSaveToStream, shlobj_core/ILSaveToStream
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
 - ILSaveToStream
 - shlobj_core/ILSaveToStream
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
 - Windows.Storage.dll
api_name:
 - ILSaveToStream
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# ILSaveToStream function


## -description

Saves an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure to a stream.

## -parameters

### -param pstm [in]

Type: <b>IStream *</b>

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface where the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> is saved.

### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A pointer to the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure to be saved.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error value otherwise.

## -remarks

The stream must be opened for writing, or <b>ILSaveToStream</b> returns an error.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-illoadfromstream">ILLoadFromStream</a>
