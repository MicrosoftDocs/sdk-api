---
UID: NE:shobjidl_core.NWMF
title: NWMF (shobjidl_core.h)
description: Flags used by INewWindowManager::EvaluateNewWindow. These values are factors in the decision of whether to display a pop-up window.
helpviewer_keywords: ["NWMF","NWMF enumeration [Windows Shell]","NWMF_FIRST","NWMF_FORCETAB","NWMF_FORCEWINDOW","NWMF_FROMDIALOGCHILD","NWMF_HTMLDIALOG","NWMF_INACTIVETAB","NWMF_OVERRIDEKEY","NWMF_SHOWHELP","NWMF_SUGGESTTAB","NWMF_SUGGESTWINDOW","NWMF_UNLOADING","NWMF_USERALLOWED","NWMF_USERINITED","NWMF_USERREQUESTED","_shell_NWMF","shell.NWMF","shobjidl_core/NWMF","shobjidl_core/NWMF_FIRST","shobjidl_core/NWMF_FORCETAB","shobjidl_core/NWMF_FORCEWINDOW","shobjidl_core/NWMF_FROMDIALOGCHILD","shobjidl_core/NWMF_HTMLDIALOG","shobjidl_core/NWMF_INACTIVETAB","shobjidl_core/NWMF_OVERRIDEKEY","shobjidl_core/NWMF_SHOWHELP","shobjidl_core/NWMF_SUGGESTTAB","shobjidl_core/NWMF_SUGGESTWINDOW","shobjidl_core/NWMF_UNLOADING","shobjidl_core/NWMF_USERALLOWED","shobjidl_core/NWMF_USERINITED","shobjidl_core/NWMF_USERREQUESTED"]
old-location: shell\NWMF.htm
tech.root: shell
ms.assetid: b55b60ae-fb56-4525-8113-35c417b28954
ms.date: 12/05/2018
ms.keywords: NWMF, NWMF enumeration [Windows Shell], NWMF_FIRST, NWMF_FORCETAB, NWMF_FORCEWINDOW, NWMF_FROMDIALOGCHILD, NWMF_HTMLDIALOG, NWMF_INACTIVETAB, NWMF_OVERRIDEKEY, NWMF_SHOWHELP, NWMF_SUGGESTTAB, NWMF_SUGGESTWINDOW, NWMF_UNLOADING, NWMF_USERALLOWED, NWMF_USERINITED, NWMF_USERREQUESTED, _shell_NWMF, shell.NWMF, shobjidl_core/NWMF, shobjidl_core/NWMF_FIRST, shobjidl_core/NWMF_FORCETAB, shobjidl_core/NWMF_FORCEWINDOW, shobjidl_core/NWMF_FROMDIALOGCHILD, shobjidl_core/NWMF_HTMLDIALOG, shobjidl_core/NWMF_INACTIVETAB, shobjidl_core/NWMF_OVERRIDEKEY, shobjidl_core/NWMF_SHOWHELP, shobjidl_core/NWMF_SUGGESTTAB, shobjidl_core/NWMF_SUGGESTWINDOW, shobjidl_core/NWMF_UNLOADING, shobjidl_core/NWMF_USERALLOWED, shobjidl_core/NWMF_USERINITED, shobjidl_core/NWMF_USERREQUESTED
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NWMF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NWMF
 - shobjidl_core/NWMF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - NWMF
---

# NWMF enumeration


## -description

Flags used by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inewwindowmanager-evaluatenewwindow">INewWindowManager::EvaluateNewWindow</a>. These values are factors in the decision of whether to display a pop-up window.

## -enum-fields

### -field NWMF_UNLOADING:0x1

The page is unloading. This flag is set in response to the <a href="/previous-versions/aa741480(v=vs.85)">onbeforeunload</a> and <a href="/previous-versions/aa741488(v=vs.85)">onunload</a> events. Some pages load pop-up windows when you leave them, not when you enter. This flag is used to identify those situations.

### -field NWMF_USERINITED:0x2

The call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inewwindowmanager-evaluatenewwindow">INewWindowManager::EvaluateNewWindow</a> is the result of a user-initiated action (a mouse click or key press). Use this flag in conjunction with the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-nwmf">NWMF_FIRST_USERINITED</a> flag to determine whether the call is a direct or indirect result of the user-initiated action.

### -field NWMF_FIRST:0x4

When <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-nwmf">NWMF_USERINITED</a> is present, this flag indicates that the call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inewwindowmanager-evaluatenewwindow">INewWindowManager::EvaluateNewWindow</a> is the first query that results from this user-initiated action. Always use this flag in conjunction with <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-nwmf">NWMF_USERINITED</a>.

### -field NWMF_OVERRIDEKEY:0x8

The override key (ALT) was pressed. The override key is used to bypass the pop-up manager—allowing all pop-up windows to display—and must be held down at the time that <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inewwindowmanager-evaluatenewwindow">INewWindowManager::EvaluateNewWindow</a> is called. 
            
                

<div class="alert"><b>Note</b>  When <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inewwindowmanager-evaluatenewwindow">INewWindowManager::EvaluateNewWindow</a> is implemented for a <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752040(v=vs.85)">WebBrowser</a> control host, the implementer can choose to ignore the override key.</div>
<div> </div>

### -field NWMF_SHOWHELP:0x10

The new window attempting to load is the result of a call to the <a href="https://developer.mozilla.org/en-US/docs/Web/API/Window">showHelp</a> method. Help is sometimes displayed in a separate window, and this flag is valuable in those cases.

### -field NWMF_HTMLDIALOG:0x20

The new window is a dialog box that displays HTML content.

### -field NWMF_FROMDIALOGCHILD:0x40

The <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inewwindowmanager-evaluatenewwindow">EvaluateNewWindow</a> method is being called from an HTML dialog. The new window should not show the UI in the parent window.

### -field NWMF_USERREQUESTED:0x80

The new windows was definitely requested by the user, either by selecting Open in New Window from a context menu or pressing Shift and clicking a link.

### -field NWMF_USERALLOWED:0x100

The call to the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inewwindowmanager-evaluatenewwindow">EvaluateNewWindow</a> method is the result of the user requesting a replay that resulted in a refresh.

### -field NWMF_FORCEWINDOW:0x10000

The new window should be forced to open in a new window rather than a tab.

### -field NWMF_FORCETAB:0x20000

The new window should be forced to open in a new tab.

### -field NWMF_SUGGESTWINDOW:0x40000

The new window should open in a new tab unless <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-nwmf">NWMF_FORCEtab</a> is also present, indicating that user wants the window to open as a window.

### -field NWMF_SUGGESTTAB:0x80000

The new window should open in a new tab unless <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-nwmf">NWMF_FORCEWINDOW</a> is also present, indicating that user wants the window to open as a window.

### -field NWMF_INACTIVETAB:0x100000

The <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inewwindowmanager-evaluatenewwindow">EvaluateNewWindow</a> method is being called from an inactive tab.
