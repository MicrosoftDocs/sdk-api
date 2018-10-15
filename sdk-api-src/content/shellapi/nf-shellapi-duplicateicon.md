---
UID: NF:shellapi.DuplicateIcon
title: DuplicateIcon function
author: windows-sdk-content
description: Creates a duplicate of a specified icon.
old-location: shell\DuplicateIcon.htm
tech.root: shell
ms.assetid: 488a24e1-f6f0-4bbd-9487-2b4c650f4879
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: DuplicateIcon, DuplicateIcon function [Windows Shell], _shell_DuplicateIcon, shell.DuplicateIcon, shellapi/DuplicateIcon
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: Shell32.dll
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
 - DuplicateIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DuplicateIcon function


## -description


Creates a duplicate of a specified icon.


## -parameters




### -param hInst [in]

Type: <b>HINSTANCE</b>


### -param hIcon [in]

Type: <b>HICON</b>

Handle to the icon to be duplicated.


## -returns



Type: <b>HICON</b>

If successful, the function returns the handle to the new icon that was created; otherwise, <b>NULL</b>.




## -remarks



When it is no longer needed, the caller is responsible for freeing the icon handle returned by <b>DuplicateIcon</b> by calling the <a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a> function.



