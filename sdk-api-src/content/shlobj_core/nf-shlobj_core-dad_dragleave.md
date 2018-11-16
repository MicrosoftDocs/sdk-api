---
UID: NF:shlobj_core.DAD_DragLeave
title: DAD_DragLeave function
author: windows-sdk-content
description: Unlocks the window locked by the DAD_DragEnterEx function.
old-location: shell\DAD_DragLeave.htm
tech.root: shell
ms.assetid: 5b2b8f04-c746-48d0-9fca-eda2c6b9ff2a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DAD_DragLeave, DAD_DragLeave function [Windows Shell], shell.DAD_DragLeave, shell_DAD_DragLeave, shlobj_core/DAD_DragLeave
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.00 or later)
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
 - DAD_DragLeave
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DAD_DragLeave
: 
---

# DAD_DragLeave function


## -description


<p class="CCE_Message">[<b>DAD_DragLeave</b> is available in Windows 2000 and Windows XP. It might be altered or unavailable in subsequent versions. Use <a href="https://msdn.microsoft.com/en-us/library/Bb761528(v=VS.85).aspx">ImageList_DragLeave</a> instead.]

Unlocks the window locked by the <a href="https://msdn.microsoft.com/32f98df7-e357-4d17-9e33-f162a6ffb7ed">DAD_DragEnterEx</a> function.



## -parameters






## -returns



Type: <b>BOOL</b>

Returns <b>SUCCEEDED</b> if successful, or <b>FALSE</b> otherwise.



