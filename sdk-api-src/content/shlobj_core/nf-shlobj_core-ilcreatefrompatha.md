---
UID: NF:shlobj_core.ILCreateFromPathA
title: ILCreateFromPathA function (shlobj_core.h)
author: windows-sdk-content
description: Returns the ITEMIDLIST structure associated with a specified file path.
old-location: shell\ILCreateFromPathW.htm
tech.root: shell
ms.assetid: dee5486c-8be9-46c1-b5a1-e917e7c1e528
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ILCreateFromPath, ILCreateFromPath function [Windows Shell], ILCreateFromPathA, ILCreateFromPathW, _win32_ILCreateFromPathW, shell.ILCreateFromPathW, shlobj_core/ILCreateFromPath, shlobj_core/ILCreateFromPathA, shlobj_core/ILCreateFromPathW
ms.topic: function
f1_keywords:
- shlobj_core/ILCreateFromPath
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Shell32.dll
- ext-ms-win-shell-shell32-l1-2-1.dll
- Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
- ILCreateFromPath
- ILCreateFromPathA
- ILCreateFromPathW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILCreateFromPathA function


## -description


Returns the <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure associated with a specified file path.


## -parameters




### -param pszPath [in]

Type: <b>PCTSTR</b>

A pointer to a null-terminated Unicode string that contains the path. This string should be no more than MAX_PATH characters in length, including the terminating null character.


## -returns



Type: <b>PIDLIST_ABSOLUTE</b>

Returns a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure that corresponds to the path.




## -remarks



Call <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree">ILFree</a> to release the <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> when you are finished with it.



