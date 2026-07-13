---
UID: NF:contentpartner.WMPNotifySubscriptionPluginAddRemove
title: WMPNotifySubscriptionPluginAddRemove function (contentpartner.h)
description: The WMPNotifySubscriptionPluginAddRemove function notifies Windows Media Player that a COM object has been installed or uninstalled.
helpviewer_keywords: ["WMPNotifyPluginAddRemove_Subscriptions","WMPNotifySubscriptionPluginAddRemove","WMPNotifySubscriptionPluginAddRemove function [Windows Media Player]","contentpartner/WMPNotifySubscriptionPluginAddRemove","wmp.wmpnotifysubscriptionpluginaddremove"]
old-location: wmp\wmpnotifysubscriptionpluginaddremove.htm
tech.root: WMP
ms.assetid: 5217142d-fe1a-4d9f-a4e4-5d9e103ee573
ms.date: 4/26/2023
ms.keywords: WMPNotifyPluginAddRemove_Subscriptions, WMPNotifySubscriptionPluginAddRemove, WMPNotifySubscriptionPluginAddRemove function [Windows Media Player], contentpartner/WMPNotifySubscriptionPluginAddRemove, wmp.wmpnotifysubscriptionpluginaddremove
req.header: contentpartner.h
req.include-header: Subscriptionservices.h
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 10 or later.
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
 - WMPNotifySubscriptionPluginAddRemove
 - contentpartner/WMPNotifySubscriptionPluginAddRemove
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - contentpartner.h
api_name:
 - WMPNotifySubscriptionPluginAddRemove
---

# WMPNotifySubscriptionPluginAddRemove function


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WMPNotifySubscriptionPluginAddRemove</b> function notifies Windows Media Player that a COM object has been installed or uninstalled.
<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div><div> </div>



## -returns

The return value indicates whether the function call succeeded.

## -remarks

This function is typically called by a plug-in in its <a href="/windows/desktop/api/olectl/nf-olectl-dllregisterserver">DllRegisterServer</a> and <a href="/windows/desktop/api/olectl/nf-olectl-dllunregisterserver">DllUnregisterServer</a> methods. It alerts Windows Media Player to enumerate registered online store objects.

## -see-also

<a href="/windows/desktop/WMP/reference-for-type-2-online-stores">Reference for Type 2 Online Stores</a>
