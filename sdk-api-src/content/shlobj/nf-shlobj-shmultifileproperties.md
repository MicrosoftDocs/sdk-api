---
UID: NF:shlobj.SHMultiFileProperties
title: SHMultiFileProperties function (shlobj.h)
description: Displays a merged property sheet for a set of files. Property values common to all the files are shown while those that differ display the string (multiple values).
helpviewer_keywords: ["SHMultiFileProperties","SHMultiFileProperties function [Windows Shell]","_win32_SHMultiFileProperties","shell.SHMultiFileProperties","shlobj/SHMultiFileProperties"]
old-location: shell\SHMultiFileProperties.htm
tech.root: shell
ms.assetid: 7c66fd91-4f7a-45f3-b849-bf210c552511
ms.date: 12/05/2018
ms.keywords: SHMultiFileProperties, SHMultiFileProperties function [Windows Shell], _win32_SHMultiFileProperties, shell.SHMultiFileProperties, shlobj/SHMultiFileProperties
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - SHMultiFileProperties
 - shlobj/SHMultiFileProperties
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
 - SHMultiFileProperties
---

# SHMultiFileProperties function


## -description

Displays a merged property sheet for a set of files. Property values common to all the files are shown while those that differ display the string <b>(multiple values)</b>.

## -parameters

### -param pdtobj [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>*</b>

A pointer to a data object that supplies the PIDLs of all of the files for which to display the merged property sheet. The data object must use the <a href="/windows/desktop/shell/clipboard">CFSTR_SHELLIDLIST</a> clipboard format. The parent folder's implementation of <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof">IShellFolder::GetDisplayNameOf</a> must return a fully qualified file system path for each item in response to the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shgdnf">SHGDN_FORPARSING</a> flag.

### -param dwFlags

Type: <b>DWORD</b>

Reserved. Must be set to 0.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/shell/clipboard">Shell Clipboard Formats</a>