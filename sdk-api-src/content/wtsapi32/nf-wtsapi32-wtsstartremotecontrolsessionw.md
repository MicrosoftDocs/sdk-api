---
UID: NF:wtsapi32.WTSStartRemoteControlSessionW
title: WTSStartRemoteControlSessionW function (wtsapi32.h)
description: Starts the remote control of another Remote Desktop Services session. You must call this function from a remote session. (Unicode)
helpviewer_keywords: ["REMOTECONTROL_KBDALT_HOTKEY", "REMOTECONTROL_KBDCTRL_HOTKEY", "REMOTECONTROL_KBDSHIFT_HOTKEY", "WTSStartRemoteControlSession", "WTSStartRemoteControlSession function [Remote Desktop Services]", "WTSStartRemoteControlSessionW", "termserv.wtsstartremotecontrolsession", "wtsapi32/WTSStartRemoteControlSession", "wtsapi32/WTSStartRemoteControlSessionW"]
old-location: termserv\wtsstartremotecontrolsession.htm
tech.root: TermServ
ms.assetid: 8ccab62b-228b-4449-82c1-970de891cbdb
ms.date: 12/05/2018
ms.keywords: REMOTECONTROL_KBDALT_HOTKEY, REMOTECONTROL_KBDCTRL_HOTKEY, REMOTECONTROL_KBDSHIFT_HOTKEY, WTSStartRemoteControlSession, WTSStartRemoteControlSession function [Remote Desktop Services], WTSStartRemoteControlSessionA, WTSStartRemoteControlSessionW, termserv.wtsstartremotecontrolsession, wtsapi32/WTSStartRemoteControlSession, wtsapi32/WTSStartRemoteControlSessionA, wtsapi32/WTSStartRemoteControlSessionW
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSStartRemoteControlSessionW (Unicode) and WTSStartRemoteControlSessionA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTSStartRemoteControlSessionW
 - wtsapi32/WTSStartRemoteControlSessionW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
api_name:
 - WTSStartRemoteControlSession
 - WTSStartRemoteControlSessionA
 - WTSStartRemoteControlSessionW
---

# WTSStartRemoteControlSessionW function


## -description

Starts the remote control of another Remote Desktop Services session. You must call this function from a remote session.

## -parameters

### -param pTargetServerName [in]

A pointer to the name of the server where the session that you want remote control of exists.

### -param TargetLogonId [in]

The logon ID of the session that you want remote control of.

### -param HotkeyVk [in]

The virtual-key code that represents the key to press to stop remote control of the session. The key that is defined in this parameter is used with the  <i>HotkeyModifiers</i> parameter.

### -param HotkeyModifiers [in]

The virtual modifier that represents the key to press to stop remote control of the session. The virtual modifier is used with the <i>HotkeyVk</i> parameter.

For example, if the <b>WTSStartRemoteControlSession</b> function is called with <i>HotkeyVk</i> set to <b>VK_MULTIPLY</b> and <i>HotkeyModifiers</i> set to <b>REMOTECONTROL_KBDCTRL_HOTKEY</b>, the user who has remote control of the target session can press CTRL + * to stop remote control of the session and return to their own session.



#### REMOTECONTROL_KBDSHIFT_HOTKEY

The SHIFT key



#### REMOTECONTROL_KBDCTRL_HOTKEY

The CTRL key



#### REMOTECONTROL_KBDALT_HOTKEY

The ALT key


##### - HotkeyModifiers.REMOTECONTROL_KBDALT_HOTKEY

The ALT key


##### - HotkeyModifiers.REMOTECONTROL_KBDCTRL_HOTKEY

The CTRL key


##### - HotkeyModifiers.REMOTECONTROL_KBDSHIFT_HOTKEY

The SHIFT key

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

> [!NOTE]
> The wtsapi32.h header defines WTSStartRemoteControlSession as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
