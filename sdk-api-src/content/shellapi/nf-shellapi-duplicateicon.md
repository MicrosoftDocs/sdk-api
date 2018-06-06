---
UID: NF:shellapi.DuplicateIcon
title: DuplicateIcon function
author: windows-sdk-content
description: Creates a duplicate of a specified icon.
old-location: menurc\duplicateicon.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\duplicateicon.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: DuplicateIcon, DuplicateIcon function [Menus and Other Resources], _win32_DuplicateIcon, _win32_duplicateicon_cpp, menurc.duplicateicon, shellapi/DuplicateIcon, winui._win32_duplicateicon
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shellapi.h
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
tech.root: 
req.typenames: SHSTOCKICONID
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
 - DuplicateIcon
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# DuplicateIcon function


## -description


Creates a duplicate of a specified icon.


## -parameters




### -param hInst

Type: <b>HINSTANCE</b>

This parameter is not used; it can be <b>NULL</b>. 


### -param hIcon [in]

Type: <b>HICON</b>

A handle to the icon to be duplicated. 


## -returns



Type: <b>HICON</b>

If successful, the function returns the handle to the new icon that was created. If unsuccessful, it returns <b>NULL</b>.




## -remarks



You must destroy the icon handle returned by <b>DuplicateIcon</b> by calling the <a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a> function.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a>



<a href="https://msdn.microsoft.com/1dc588f4-b032-40a8-82ef-5b9fc04abb0b">Icons</a>



<b>Reference</b>
 

 

