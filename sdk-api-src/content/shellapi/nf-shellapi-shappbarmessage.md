---
UID: NF:shellapi.SHAppBarMessage
title: SHAppBarMessage function (shellapi.h)
description: Sends an appbar message to the system.
helpviewer_keywords: ["ABM_ACTIVATE","ABM_GETAUTOHIDEBAR","ABM_GETAUTOHIDEBAREX","ABM_GETSTATE","ABM_GETTASKBARPOS","ABM_NEW","ABM_QUERYPOS","ABM_REMOVE","ABM_SETAUTOHIDEBAR","ABM_SETAUTOHIDEBAREX","ABM_SETPOS","ABM_SETSTATE","ABM_WINDOWPOSCHANGED","SHAppBarMessage","SHAppBarMessage function [Windows Shell]","_win32_SHAppBarMessage","shell.SHAppBarMessage","shellapi/SHAppBarMessage"]
old-location: shell\SHAppBarMessage.htm
tech.root: shell
ms.assetid: 173d6eff-b33b-4d7d-bedd-5ebfb1e45954
ms.date: 12/05/2018
ms.keywords: ABM_ACTIVATE, ABM_GETAUTOHIDEBAR, ABM_GETAUTOHIDEBAREX, ABM_GETSTATE, ABM_GETTASKBARPOS, ABM_NEW, ABM_QUERYPOS, ABM_REMOVE, ABM_SETAUTOHIDEBAR, ABM_SETAUTOHIDEBAREX, ABM_SETPOS, ABM_SETSTATE, ABM_WINDOWPOSCHANGED, SHAppBarMessage, SHAppBarMessage function [Windows Shell], _win32_SHAppBarMessage, shell.SHAppBarMessage, shellapi/SHAppBarMessage
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHAppBarMessage
 - shellapi/SHAppBarMessage
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
 - SHAppBarMessage
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# SHAppBarMessage function


## -description

Sends an appbar message to the system.

## -parameters

### -param dwMessage [in]

Type: <b>DWORD</b>

Appbar message value to send. This parameter can be one of the following values.



#### ABM_NEW (0x00000000)

Registers a new appbar and specifies the message identifier that the system should use to send notification messages to the appbar.



#### ABM_REMOVE (0x00000001)

Unregisters an appbar, removing the bar from the system's internal list.



#### ABM_QUERYPOS (0x00000002)

Requests a size and screen position for an appbar.



#### ABM_SETPOS (0x00000003)

Sets the size and screen position of an appbar.



#### ABM_GETSTATE (0x00000004)

Retrieves the autohide and always-on-top states of the Windows taskbar.



#### ABM_GETTASKBARPOS (0x00000005)

Retrieves the bounding rectangle of the Windows taskbar. Note that this applies only to the system taskbar. Other objects, particularly toolbars supplied with third-party software, also can be present. As a result, some of the screen area not covered by the Windows taskbar might not be visible to the user. To retrieve the area of the screen not covered by both the taskbar and other app bars—the working area available to your application—, use the <a href="/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa">GetMonitorInfo</a> function.



#### ABM_ACTIVATE (0x00000006)

Notifies the system to activate or deactivate an appbar. The <b>lParam</b> member of the <a href="/windows/desktop/api/shellapi/ns-shellapi-appbardata">APPBARDATA</a> pointed to by <i>pData</i> is set to <b>TRUE</b> to activate or <b>FALSE</b> to deactivate.



#### ABM_GETAUTOHIDEBAR (0x00000007)

Retrieves the handle to the autohide appbar associated with a particular edge of the screen.



#### ABM_SETAUTOHIDEBAR (0x00000008)

Registers or unregisters an autohide appbar for an edge of the screen.



#### ABM_WINDOWPOSCHANGED (0x00000009)

Notifies the system when an appbar's position has changed.



#### ABM_SETSTATE (0x0000000A)

<b>Windows XP and later:</b> Sets the state of the appbar's autohide and always-on-top attributes.



#### ABM_GETAUTOHIDEBAREX (0x0000000B)

<b>Windows XP and later:</b> Retrieves the handle to the autohide appbar associated with a particular edge of a particular monitor.



#### ABM_SETAUTOHIDEBAREX (0x0000000C)

<b>Windows XP and later:</b> Registers or unregisters an autohide appbar for an edge of a particular monitor.

### -param pData [in, out]

Type: <b>PAPPBARDATA</b>

A pointer to an <a href="/windows/desktop/api/shellapi/ns-shellapi-appbardata">APPBARDATA</a> structure. The content of the structure on entry and on exit depends on the value set in the <i>dwMessage</i> parameter. See the individual message pages for specifics.

## -returns

Type: <b>UINT_PTR</b>

This function returns a message-dependent value. For more information, see the Windows SDK documentation for the specific appbar message sent. Links to those documents are given in the See Also section.

## -see-also

<a href="/windows/desktop/shell/abm-activate">ABM_ACTIVATE</a>



<a href="/windows/desktop/shell/abm-getautohidebar">ABM_GETAUTOHIDEBAR</a>



<a href="/windows/desktop/shell/abm-getautohidebarex">ABM_GETAUTOHIDEBAREX</a>



<a href="/windows/desktop/shell/abm-getstate">ABM_GETSTATE</a>



<a href="/windows/desktop/shell/abm-gettaskbarpos">ABM_GETTASKBARPOS</a>



<a href="/windows/desktop/shell/abm-new">ABM_NEW</a>



<a href="/windows/desktop/shell/abm-querypos">ABM_QUERYPOS</a>



<a href="/windows/desktop/shell/abm-remove">ABM_REMOVE</a>



<a href="/windows/desktop/shell/abm-setautohidebar">ABM_SETAUTOHIDEBAR</a>



<a href="/windows/desktop/shell/abm-setautohidebarex">ABM_SETAUTOHIDEBAREX</a>



<a href="/windows/desktop/shell/abm-setpos">ABM_SETPOS</a>



<a href="/windows/desktop/shell/abm-setstate">ABM_SETSTATE</a>



<a href="/windows/desktop/shell/abm-windowposchanged">ABM_WINDOWPOSCHANGED</a>
