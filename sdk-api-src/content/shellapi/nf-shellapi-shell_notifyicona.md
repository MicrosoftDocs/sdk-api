---
UID: NF:shellapi.Shell_NotifyIconA
title: Shell_NotifyIconA function (shellapi.h)
description: Sends a message to the taskbar's status area. (ANSI)
helpviewer_keywords: ["NIM_ADD", "NIM_DELETE", "NIM_MODIFY", "NIM_SETFOCUS", "NIM_SETVERSION", "Shell_NotifyIconA", "shellapi/Shell_NotifyIconA"]
old-location: shell\Shell_NotifyIcon.htm
tech.root: shell
ms.assetid: a316bc29-5f19-4a04-a32b-f4caeea0c029
ms.date: 12/05/2018
ms.keywords: NIM_ADD, NIM_DELETE, NIM_MODIFY, NIM_SETFOCUS, NIM_SETVERSION, Shell_NotifyIcon, Shell_NotifyIcon function [Windows Shell], Shell_NotifyIconA, Shell_NotifyIconW, _win32_Shell_NotifyIcon, shell.Shell_NotifyIcon, shellapi/Shell_NotifyIcon, shellapi/Shell_NotifyIconA, shellapi/Shell_NotifyIconW
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: Shell_NotifyIconW (Unicode) and Shell_NotifyIconA (ANSI)
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
 - Shell_NotifyIconA
 - shellapi/Shell_NotifyIconA
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
 - Shell_NotifyIcon
 - Shell_NotifyIconA
 - Shell_NotifyIconW
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# Shell_NotifyIconA function


## -description

Sends a message to the taskbar's status area.

## -parameters

### -param dwMessage [in]

Type: <b>DWORD</b>

A value that specifies the action to be taken by this function. It can have one of the following values:



#### NIM_ADD (0x00000000)

0x00000000. Adds an icon to the status area. The icon is given an identifier in the <a href="/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa">NOTIFYICONDATA</a> structure pointed to by <i>lpdata</i>—either through its <b>uID</b> or <b>guidItem</b> member. This identifier is used in subsequent calls to <b>Shell_NotifyIcon</b> to perform later actions on the icon.



#### NIM_MODIFY (0x00000001)

0x00000001. Modifies an icon in the status area. <a href="/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa">NOTIFYICONDATA</a> structure pointed to by <i>lpdata</i> uses the ID originally assigned to the icon when it was added to the notification area (NIM_ADD) to identify the icon to be modified.



#### NIM_DELETE (0x00000002)

0x00000002. Deletes an icon from the status area. <a href="/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa">NOTIFYICONDATA</a> structure pointed to by <i>lpdata</i> uses the ID originally assigned to the icon when it was added to the notification area (NIM_ADD) to identify the icon to be deleted.



#### NIM_SETFOCUS (0x00000003)

0x00000003. <a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Shell32.dll version 5.0 and later only</a>. Returns focus to the taskbar notification area. Notification area icons should use this message when they have completed their UI operation. For example, if the icon displays a shortcut menu, but the user presses ESC to cancel it, use <b>NIM_SETFOCUS</b> to return focus to the notification area.



#### NIM_SETVERSION (0x00000004)

0x00000004. <a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Shell32.dll version 5.0 and later only</a>. Instructs the notification area to behave according to the version number specified in the <b>uVersion</b> member of the structure pointed to by <i>lpdata</i>. The version number specifies which members are recognized.

NIM_SETVERSION must be called every time a notification area icon is added (NIM_ADD). It does not need to be called with NIM_MODIFY. The version setting is not persisted once a user logs off.

For details, see the Remarks section.

### -param lpData [in]

Type: <b>PNOTIFYICONDATA</b>

A pointer to a <a href="/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa">NOTIFYICONDATA</a> structure. The content of the structure depends on the value of <i>dwMessage</i>. It can define an icon to add to the notification area, cause that icon to display a notification, or identify an icon to modify or delete.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. If <i>dwMessage</i> is set to NIM_SETVERSION, the function returns <b>TRUE</b> if the version was successfully changed, or <b>FALSE</b> if the requested version is not supported.

## -remarks

As of Windows 2000 (<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Shell32.dll version 5.0</a>), if you set the <b>uVersion</b> member of the <a href="/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa">NOTIFYICONDATA</a> structure pointed to by <i>lpdata</i> to NOTIFYICON_VERSION_4 or higher, <b>Shell_NotifyIcon</b> mouse and keyboard events are handled differently than in earlier versions of Windows. The differences include the following:

<ul>
<li>If a user selects a notify icon's shortcut menu with the keyboard, the Shell now sends the associated application a <a href="/windows/desktop/menurc/wm-contextmenu">WM_CONTEXTMENU</a> message. Earlier versions send <a href="/windows/desktop/inputdev/wm-rbuttondown">WM_RBUTTONDOWN</a> and <a href="/windows/desktop/inputdev/wm-rbuttonup">WM_RBUTTONUP</a> messages.</li>
<li>If a user selects a notify icon with the keyboard and activates it with the SPACEBAR or ENTER key, the version 5.0 Shell sends the associated application an NIN_KEYSELECT notification. Earlier versions send <a href="/windows/desktop/inputdev/wm-rbuttondown">WM_RBUTTONDOWN</a> and <a href="/windows/desktop/inputdev/wm-rbuttonup">WM_RBUTTONUP</a> messages.</li>
<li>If a user selects a notify icon with the mouse and activates it with the ENTER key, the Shell now sends the associated application an NIN_SELECT notification. Earlier versions send <a href="/windows/desktop/inputdev/wm-rbuttondown">WM_RBUTTONDOWN</a> and <a href="/windows/desktop/inputdev/wm-rbuttonup">WM_RBUTTONUP</a> messages.</li>
</ul>
As of Windows XP (<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Shell32.dll version 6.0</a>), if a user passes the mouse pointer over an icon with which a balloon notification is associated, the Shell sends the following messages:

<ul>
<li>NIN_BALLOONSHOW. Sent when the balloon is shown (balloons are queued).</li>
<li>
NIN_BALLOONHIDE. Sent when the balloon disappears. For example, when the icon is deleted. This message is not sent if the balloon is dismissed because of a timeout or if the user clicks the mouse.

As of Windows 7, NIN_BALLOONHIDE is also sent when a notification with the <a href="/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa">NIIF_RESPECT_QUIET_TIME</a> flag set attempts to display during quiet time (a user's first hour on a new computer). In that case, the balloon is never displayed at all.

</li>
<li>NIN_BALLOONTIMEOUT. Sent when the balloon is dismissed because of a timeout.</li>
<li>NIN_BALLOONUSERCLICK. Sent when the balloon is dismissed because the user clicked the mouse.</li>
</ul>
In addition to those messages, as of Windows Vista (Shell32.dll version 6.0.6), if a user passes the mouse pointer over an icon with which a balloon notification is associated, the Windows Vista Shell also adds the following messages:

<ul>
<li>NIN_POPUPOPEN. Sent when the user hovers the cursor over an icon to indicate that the richer pop-up UI should be used in place of a standard textual tooltip.</li>
<li>NIN_POPUPCLOSE. Sent when a cursor no longer hovers over an icon to indicate that the rich pop-up UI should be closed.</li>
</ul>
Regardless of the operating system version, you can select which way the Shell should behave by calling <b>Shell_NotifyIcon</b> with <i>dwMessage</i> set to <b>NIM_SETVERSION</b>. Set the <b>uVersion</b> member of the <a href="/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa">NOTIFYICONDATA</a> structure pointed to by <i>lpdata</i> to indicate whether you want Windows 2000, Windows Vista, or pre-version 5.0 (Windows 95) behavior.

<div class="alert"><b>Note</b>  The messages discussed above are not conventional Windows messages. They are sent as the <i>lParam</i> value of the application-defined message that is specified in the <b>uCallbackMessage</b> member of the <a href="/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa">NOTIFYICONDATA</a> structure pointed to by <i>lpdata</i>, when <b>Shell_NotifyIcon</b> is called with the <b>NIM_ADD</b> flag set in <i>dwMessage</i>.</div>
<div> </div>
As of Windows XP Service Pack 2 (SP2), a custom icon can be displayed in the notification balloon. This allows the calling process to customize the notification beyond the previously available options of info, warning, and error, and distinguish it from other types of notification for the user.





> [!NOTE]
> The shellapi.h header defines Shell_NotifyIcon as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/shell/notification-area">Notifications and the Notification Area</a>
