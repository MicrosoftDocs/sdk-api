---
UID: NF:shlobj_core.PathMakeUniqueName
title: PathMakeUniqueName function
author: windows-driver-content
description: Creates a unique path name from a template.
old-location: shell\PathMakeUniqueName.htm
old-project: shell
ms.assetid: 8456ae0c-e83c-43d0-a86a-1861a373d237
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: PathMakeUniqueName, PathMakeUniqueName function [Windows Shell], _win32_PathMakeUniqueName, shell.PathMakeUniqueName, shlobj_core/PathMakeUniqueName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shell32.dll
-	Ext-MS-Win-Shell32-ShellFolders-l1-1-1.dll
-	FolderExt.dll
-	windows.storage.dll
api_name:
-	PathMakeUniqueName
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# PathMakeUniqueName function


## -description


Creates a unique path name from a template.


## -parameters




### -param pszUniqueName [out]

Type: <b>PWSTR</b>

A buffer that receives a null-terminated Unicode string that contains the unique path name. It should be at least MAX_PATH characters in length.


### -param cchMax

Type: <b>UINT</b>

The number of characters in the buffer pointed to by <i>pszUniqueName</i>.


### -param pszTemplate [in]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that contains a template that is used to construct the unique name. This template is used for drives that require file names with the 8.3 format. This string should be no more than MAX_PATH characters in length, including the terminating null character.


### -param pszLongPlate [in, optional]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that contains a template that is used to construct the unique name. This template is used for drives that support long file names. This string should be no more than MAX_PATH characters in length, including the terminating null character.


### -param pszDir [in, optional]

Type: <b>PCWSTR</b>

A null-terminated string that contains the directory in which the new file resides. This string should be no more than MAX_PATH characters in length, including the terminating null character.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful; otherwise, <b>FALSE</b>.




## -remarks



This function generates a new unique file name based on the templates specified by <i>pszTemplate</i>, for drives that require the 8.3 format, and <i>pszLongPlate</i> for drives that support long file names. For example, if you specify "My New Filename" for <i>pszLongPlate</i>, <b>PathMakeUniqueName</b> returns names such as "My New Filename (1)", "My New Filename (2)", and so on.



