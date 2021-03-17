---
UID: NF:shlobj_core.PifMgr_OpenProperties
title: PifMgr_OpenProperties function (shlobj_core.h)
description: Opens the .pif file associated with a Microsoft MS-DOS application, and returns a handle to the application's properties.
helpviewer_keywords: ["OPENPROPS_INHIBITPIF","OPENPROPS_NONE","PifMgr_OpenProperties","PifMgr_OpenProperties function [Windows Properties]","_win32_PifMgr_OpenProperties","properties.PifMgr_OpenProperties","shell.PifMgr_OpenProperties","shlobj_core/PifMgr_OpenProperties"]
old-location: properties\PifMgr_OpenProperties.htm
tech.root: properties
ms.assetid: 0bc11528-7278-4765-b3cb-671ba82c9155
ms.date: 12/05/2018
ms.keywords: OPENPROPS_INHIBITPIF, OPENPROPS_NONE, PifMgr_OpenProperties, PifMgr_OpenProperties function [Windows Properties], _win32_PifMgr_OpenProperties, properties.PifMgr_OpenProperties, shell.PifMgr_OpenProperties, shlobj_core/PifMgr_OpenProperties
req.header: shlobj_core.h
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
 - PifMgr_OpenProperties
 - shlobj_core/PifMgr_OpenProperties
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
 - PifMgr_OpenProperties
---

# PifMgr_OpenProperties function


## -description

<p class="CCE_Message">[<b>PifMgr_OpenProperties</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Opens the .pif file associated with a Microsoft MS-DOS application, and returns a handle to the application's properties.

## -parameters

### -param pszApp [in]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that contains the application's name.

### -param pszPIF [in, optional]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that contains the name of the .pif file.

### -param hInf

Type: <b>UINT</b>

A handle to the application's .inf file. Set this value to zero if there is no .inf file. Set this value to -1 to prevent the .inf file from being processed.

### -param flOpt

Type: <b>UINT</b>

A flag that controls how the function operates.



#### OPENPROPS_INHIBITPIF

Ignore any existing .pif files and get the properties from win.ini or _Default.pif. This flag is ignored on Windows NT, Windows 2000, and Windows XP.
					



#### OPENPROPS_NONE

No options specified.

## -returns

Type: <b>HANDLE</b>

Returns a handle to the application's properties. Use this handle when you call the related .pif functions.

## -remarks

You should not think of <b>PifMgr_OpenProperties</b> as a function that opens a file somewhere. The .pif file does not remain open after this call. It is more useful to think of the function as a property structure allocator that you can initialize using disk data. 
The primary reason why this function fails is because of low memory or inability to open the specified .pif file.

If no .pif file exists, the function still allocates a data block in memory and initializes it with data from _Default.pif or its internal defaults.  If the function looks for a .pif file name but does not find it, it constructs a name and saves it in its internal .pif data structure. This guarantees that if <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pifmgr_setproperties">PifMgr_SetProperties</a> is called, the data is saved to disk.

If the function does not find the .pif file, it searches for it in the following order. 

				

<ol>
<li>Searches the current directory.</li>
<li>Searches the specified directory.</li>
<li>Searches in .pif directory.</li>
<li>Searches the folders specified by the PATH environment variable.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pifmgr_closeproperties">PifMgr_CloseProperties</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pifmgr_getproperties">PifMgr_GetProperties</a>