---
UID: NF:shlobj_core.SHFindFiles
title: SHFindFiles function (shlobj_core.h)
description: SHFindFiles may be altered or unavailable.
helpviewer_keywords: ["SHFindFiles","SHFindFiles function [Windows Shell]","_win32_SHFindFiles","shell.SHFindFiles","shlobj_core/SHFindFiles"]
old-location: shell\SHFindFiles.htm
tech.root: shell
ms.assetid: c54036c2-e6b9-4b21-b2b2-a6721c502ee5
ms.date: 12/05/2018
ms.keywords: SHFindFiles, SHFindFiles function [Windows Shell], _win32_SHFindFiles, shell.SHFindFiles, shlobj_core/SHFindFiles
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
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHFindFiles
 - shlobj_core/SHFindFiles
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
 - SHFindFiles
---

# SHFindFiles function


## -description

<p class="CCE_Message">[<b>SHFindFiles</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Displays the <b>Search</b> window UI.

## -parameters

### -param pidlFolder [in, optional]

Type: <b>PCIDLIST_ABSOLUTE</b>

The folder from which to start the search. This folder appears in the <b>Look in:</b> box in the <b>Search</b> window. This folder and all of its subfolders are searched unless users choose other options in the <b>Search</b> window's <b>More Advanced Options</b>. This value can be <b>NULL</b>.

### -param pidlSaveFile [in, optional]

Type: <b>PCIDLIST_ABSOLUTE</b>

This parameter is not used and must be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>A saved search file (.fnd) to load. You can save search parameters to a .fnd file after the search is begun. This value can be <b>NULL</b>.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful in displaying the <b>Search</b> window; otherwise <b>FALSE</b>.

