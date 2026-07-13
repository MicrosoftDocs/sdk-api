---
UID: NF:winuser.CallMsgFilterA
title: CallMsgFilterA function (winuser.h)
description: Passes the specified message and hook code to the hook procedures associated with the WH_SYSMSGFILTER and WH_MSGFILTER hooks. (ANSI)
helpviewer_keywords: ["CallMsgFilterA", "winuser/CallMsgFilterA"]
old-location: winmsg\callmsgfilter.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookfunctions\callmsgfilter.htm
ms.date: 12/05/2018
ms.keywords: CallMsgFilter, CallMsgFilter function [Windows and Messages], CallMsgFilterA, CallMsgFilterW, _win32_CallMsgFilter, _win32_callmsgfilter_cpp, winmsg.callmsgfilter, winui._win32_callmsgfilter, winuser/CallMsgFilter, winuser/CallMsgFilterA, winuser/CallMsgFilterW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CallMsgFilterW (Unicode) and CallMsgFilterA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CallMsgFilterA
 - winuser/CallMsgFilterA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-message-l1-1-0.dll
 - Ext-MS-Win-NTUser-message-l1-1-1.dll
 - Ext-MS-Win-NTUser-Message-l1-1-2.dll
 - Ext-MS-Win-NTUser-Message-L1-1-3.dll
api_name:
 - CallMsgFilter
 - CallMsgFilterA
 - CallMsgFilterW
req.apiset: ext-ms-win-ntuser-message-l1-1-0 (introduced in Windows 8)
---

# CallMsgFilterA function


## -description

Passes the specified message and hook code to the hook procedures associated with the <a href="/windows/desktop/winmsg/about-hooks">WH_SYSMSGFILTER and WH_MSGFILTER</a> hooks. A <b>WH_SYSMSGFILTER</b> or <b>WH_MSGFILTER</b> hook procedure is an application-defined callback function that examines and, optionally, modifies messages for a dialog box, message box, menu, or scroll bar.

## -parameters

### -param lpMsg [in]

Type: <b>LPMSG</b>

A pointer to an <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure that contains the message to be passed to the hook procedures.

### -param nCode [in]

Type: <b>int</b>

An application-defined code used by the hook procedure to determine how to process the message. The code must not have the same value as system-defined hook codes (MSGF_ and HC_) associated with the <a href="/windows/desktop/winmsg/about-hooks">WH_SYSMSGFILTER</a> and <b>WH_MSGFILTER</b> hooks.

## -returns

Type: <b>BOOL</b>

If the application should process the message further, the return value is zero.

If the application should not process the message further, the return value is nonzero.

## -remarks

The system calls <b>CallMsgFilter</b> to enable applications to examine and control the flow of messages during internal processing of dialog boxes, message boxes, menus, and scroll bars, or when the user activates a different window by pressing the ALT+TAB key combination. 

Install this hook procedure by using the <a href="/windows/desktop/api/winuser/nf-winuser-setwindowshookexa">SetWindowsHookEx</a> function. 


#### Examples

For an example, see <a href="/windows/desktop/winmsg/about-hooks">WH_MSGFILTER and WH_SYSMSGFILTER Hooks</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines CallMsgFilter as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/winmsg/hooks">Hooks</a>



<a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a>



<a href="/windows/win32/winmsg/messageproc">MessageProc</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowshookexa">SetWindowsHookEx</a>



<a href="/windows/win32/winmsg/sysmsgproc">SysMsgProc</a>
