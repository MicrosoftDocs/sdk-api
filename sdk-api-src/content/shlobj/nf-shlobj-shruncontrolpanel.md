---
UID: NF:shlobj.SHRunControlPanel
title: SHRunControlPanel function (shlobj.h)
description: Opens a Control Panel item.
helpviewer_keywords: ["SHRunControlPanel","SHRunControlPanel function [Windows Shell]","_shell_SHRunControlPanel","shell.SHRunControlPanel","shlobj/SHRunControlPanel"]
old-location: shell\SHRunControlPanel.htm
tech.root: shell
ms.assetid: 393a1f63-071e-4655-b6fb-7b0abca7818c
ms.date: 12/05/2018
ms.keywords: SHRunControlPanel, SHRunControlPanel function [Windows Shell], _shell_SHRunControlPanel, shell.SHRunControlPanel, shlobj/SHRunControlPanel
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHRunControlPanel
 - shlobj/SHRunControlPanel
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
 - SHRunControlPanel
---

# SHRunControlPanel function


## -description

Opens a Control Panel item.
            
<div class="alert"><b>Note</b>  This function is not supported as of Windows Vista</div><div> </div>

## -parameters

### -param lpcszCmdLine [in]

Type: <b>PCWSTR</b>

Pointer to a string that contains the command line that opens the Control Panel item. This command line includes at least the name of the .cpl file. It can also contain any other necessary information such as the property sheet page within the item (either by ordinal or by name). For more information, see <a href="/windows/desktop/shell/executing-control-panel-items">Executing Control Panel Items</a>.

### -param hwndMsgParent [in, optional]

Type: <b>HWND</b>

The handle of the parent window, used to display error messages about the opening of the item. This value can be <b>NULL</b>.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if the Control Panel item was opened successfully; otherwise, <b>FALSE</b>. 

                    

As of Windows Vista, this function always returns <b>FALSE</b>.

## -remarks

If the specified Control Panel item is already running, <b>SHRunControlPanel</b> attempts to switch to that instance rather than opening a new instance.


#### Examples

Example calls to <b>SHRunControlPanel</b> are shown here.


``` syntax
SHRunControlPanel(TEXT("timedate.cpl"), hwnd);
SHRunControlPanel(L"appwiz.cpl", NULL);
SHRunControlPanel(L"appwiz.cpl,2", NULL);
SHRunControlPanel("desk.cpl,Settings", hwnd
```

