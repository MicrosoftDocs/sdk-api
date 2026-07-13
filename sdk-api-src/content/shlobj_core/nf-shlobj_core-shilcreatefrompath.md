---
UID: NF:shlobj_core.SHILCreateFromPath
title: SHILCreateFromPath function (shlobj_core.h)
description: SHILCreateFromPath may be altered or unavailable.
helpviewer_keywords: ["SHILCreateFromPath","SHILCreateFromPath function [Windows Shell]","_win32_SHILCreateFromPath","shell.SHILCreateFromPath","shlobj_core/SHILCreateFromPath"]
old-location: shell\SHILCreateFromPath.htm
tech.root: shell
ms.assetid: 08700af7-9dbd-4162-8578-bfa47e3db6bf
ms.date: 12/05/2018
ms.keywords: SHILCreateFromPath, SHILCreateFromPath function [Windows Shell], _win32_SHILCreateFromPath, shell.SHILCreateFromPath, shlobj_core/SHILCreateFromPath
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
 - SHILCreateFromPath
 - shlobj_core/SHILCreateFromPath
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
 - SHILCreateFromPath
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# SHILCreateFromPath function


## -description

<p class="CCE_Message">[<b>SHILCreateFromPath</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Applications should use <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shparsedisplayname">SHParseDisplayName</a> instead]

Creates a pointer to an item identifier list (PIDL) from a path.

## -parameters

### -param pszPath [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH containing the path to be converted.

### -param ppidl [out]

Type: <b>PIDLIST_ABSOLUTE*</b>

The path in <i>pszPath</i> expressed as a PIDL.

### -param rgfInOut [in, out, optional]

Type: <b>DWORD*</b>

A pointer to a <b>DWORD</b> value that, on entry, indicates any attributes of the folder named in <i>pszPath</i> that the calling application would like to retrieve along with the PIDL. On exit, this value contains those requested attributes. For a list of possible attribute flags for this parameter, see <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof">IShellFolder::GetAttributesOf</a>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
