---
UID: NF:wmpplug.WMPNotifyPluginAddRemove
title: WMPNotifyPluginAddRemove function (wmpplug.h)
description: The WMPNotifyPluginAddRemove function notifies Windows Media Player that a plug-in has been installed or uninstalled.
helpviewer_keywords: ["WMPNotifyPluginAddRemove","WMPNotifyPluginAddRemove function [Windows Media Player]","wmp.wmpnotifypluginaddremove","wmpplug/WMPNotifyPluginAddRemove"]
old-location: wmp\wmpnotifypluginaddremove.htm
tech.root: WMP
ms.assetid: e367011a-2151-4324-90da-304dd7f989ab
ms.date: 4/26/2023
ms.keywords: WMPNotifyPluginAddRemove, WMPNotifyPluginAddRemove function [Windows Media Player], wmp.wmpnotifypluginaddremove, wmpplug/WMPNotifyPluginAddRemove
req.header: wmpplug.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMPNotifyPluginAddRemove
 - wmpplug/WMPNotifyPluginAddRemove
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmpplug.h
api_name:
 - WMPNotifyPluginAddRemove
---

# WMPNotifyPluginAddRemove function


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WMPNotifyPluginAddRemove</b> function notifies Windows Media Player that a plug-in has been installed or uninstalled.



## -returns

The return value indicates whether the function call succeeded.

## -remarks

This function is typically called by a user interface (UI) plug-in in its <a href="/windows/desktop/api/olectl/nf-olectl-dllregisterserver">DllRegisterServer</a> and <a href="/windows/desktop/api/olectl/nf-olectl-dllunregisterserver">DllUnregisterServer</a> methods. Windows Media Player Plug-in Wizard generates this code automatically, so it is only necessary to add calls to this function to UI plug-ins created without the wizard.

## -see-also

<a href="/windows/desktop/WMP/user-interface-plug-ins-programming-reference">User Interface Plug-ins Programming Reference</a>
