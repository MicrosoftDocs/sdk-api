---
UID: NE:exdisp.ShellWindowTypeConstants
title: ShellWindowTypeConstants (exdisp.h)
description: Specifies types of Shell windows.
helpviewer_keywords: ["SWC_3RDPARTY","SWC_BROWSER","SWC_CALLBACK","SWC_DESKTOP","SWC_EXPLORER","ShellWindowTypeConstants","ShellWindowTypeConstants enumeration [Windows Shell]","_win32_ShellWindowTypeConstants","exdisp/SWC_3RDPARTY","exdisp/SWC_BROWSER","exdisp/SWC_CALLBACK","exdisp/SWC_DESKTOP","exdisp/SWC_EXPLORER","exdisp/ShellWindowTypeConstants","shell.ShellWindowTypeConstants"]
old-location: shell\ShellWindowTypeConstants.htm
tech.root: shell
ms.assetid: 79d4fcf3-5256-4e21-ab9a-94605e1d742f
ms.date: 12/05/2018
ms.keywords: SWC_3RDPARTY, SWC_BROWSER, SWC_CALLBACK, SWC_DESKTOP, SWC_EXPLORER, ShellWindowTypeConstants, ShellWindowTypeConstants enumeration [Windows Shell], _win32_ShellWindowTypeConstants, exdisp/SWC_3RDPARTY, exdisp/SWC_BROWSER, exdisp/SWC_CALLBACK, exdisp/SWC_DESKTOP, exdisp/SWC_EXPLORER, exdisp/ShellWindowTypeConstants, shell.ShellWindowTypeConstants
req.header: exdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Exdisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ShellWindowTypeConstants
req.redist: 
req.product: Internet Explorer 5
ms.custom: 19H1
f1_keywords:
 - ShellWindowTypeConstants
 - exdisp/ShellWindowTypeConstants
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Exdisp.h
api_name:
 - ShellWindowTypeConstants
---

# ShellWindowTypeConstants enumeration


## -description

Specifies types of Shell windows.

## -enum-fields

### -field SWC_EXPLORER:0

An Windows Explorer (Explorer.exe) window.

### -field SWC_BROWSER:0x1

An Internet Explorer (Iexplore.exe) browser window.

### -field SWC_3RDPARTY:0x2

A non-Microsoft browser window.

### -field SWC_CALLBACK:0x4

A creation callback window.

### -field SWC_DESKTOP:0x8

<b>Windows Vista and later</b>. The Windows desktop.

## -see-also

<a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice-registerwindow">IBrowserService::RegisterWindow</a>



<a href="/windows/desktop/api/exdisp/nn-exdisp-ishellwindows">IShellWindows</a>



<a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-findwindowsw">IShellWindows::FindWindowSW</a>



<a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-register">IShellWindows::Register</a>



<a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-registerpending">IShellWindows::RegisterPending</a>
