---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



