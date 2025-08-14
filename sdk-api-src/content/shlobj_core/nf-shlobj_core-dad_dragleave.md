---
UID: NF:shlobj_core.DAD_DragLeave
title: DAD_DragLeave function (shlobj_core.h)
description: Unlocks the window locked by the DAD_DragEnterEx function.
helpviewer_keywords: ["DAD_DragLeave","DAD_DragLeave function [Windows Shell]","shell.DAD_DragLeave","shell_DAD_DragLeave","shlobj_core/DAD_DragLeave"]
old-location: shell\DAD_DragLeave.htm
tech.root: shell
ms.assetid: 5b2b8f04-c746-48d0-9fca-eda2c6b9ff2a
ms.date: 12/05/2018
ms.keywords: DAD_DragLeave, DAD_DragLeave function [Windows Shell], shell.DAD_DragLeave, shell_DAD_DragLeave, shlobj_core/DAD_DragLeave
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DAD_DragLeave
 - shlobj_core/DAD_DragLeave
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
 - DAD_DragLeave
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# DAD_DragLeave function


## -description

<p class="CCE_Message">[<b>DAD_DragLeave</b> is available in Windows 2000 and Windows XP. It might be altered or unavailable in subsequent versions. Use <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_dragleave">ImageList_DragLeave</a> instead.]

Unlocks the window locked by the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-dad_dragenterex">DAD_DragEnterEx</a> function.



## -returns

Type: <b>BOOL</b>

Returns <b>SUCCEEDED</b> if successful, or <b>FALSE</b> otherwise.
