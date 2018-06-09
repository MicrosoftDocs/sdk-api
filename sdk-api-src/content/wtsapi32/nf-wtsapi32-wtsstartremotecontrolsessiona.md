---
UID: NF:wtsapi32.WTSStartRemoteControlSessionA
title: WTSStartRemoteControlSessionA function
author: windows-sdk-content
description: Starts the remote control of another Remote Desktop Services session. You must call this function from a remote session.
old-location: termserv\wtsstartremotecontrolsession.htm
old-project: TermServ
ms.assetid: 8ccab62b-228b-4449-82c1-970de891cbdb
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: REMOTECONTROL_KBDALT_HOTKEY, REMOTECONTROL_KBDCTRL_HOTKEY, REMOTECONTROL_KBDSHIFT_HOTKEY, WTSStartRemoteControlSession, WTSStartRemoteControlSession function [Remote Desktop Services], WTSStartRemoteControlSessionA, WTSStartRemoteControlSessionW, termserv.wtsstartremotecontrolsession, wtsapi32/WTSStartRemoteControlSession, wtsapi32/WTSStartRemoteControlSessionA, wtsapi32/WTSStartRemoteControlSessionW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WTS_VIRTUAL_CLASS
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
product: Windows
targetos: Windows
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WTSStartRemoteControlSessionA function


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


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



