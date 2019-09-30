---
UID: NF:subscriptionservices.WMPNotifySubscriptionPluginAddRemove
title: WMPNotifySubscriptionPluginAddRemove function (subscriptionservices.h)
author: windows-sdk-content
description: The WMPNotifySubscriptionPluginAddRemove function notifies Windows Media Player that a COM object has been installed or uninstalled.
old-location: wmp\wmpnotifysubscriptionpluginaddremove.htm
tech.root: WMP
ms.assetid: 5217142d-fe1a-4d9f-a4e4-5d9e103ee573
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WMPNotifyPluginAddRemove_Subscriptions, WMPNotifySubscriptionPluginAddRemove, WMPNotifySubscriptionPluginAddRemove function [Windows Media Player], contentpartner/WMPNotifySubscriptionPluginAddRemove, wmp.wmpnotifysubscriptionpluginaddremove
ms.topic: function
f1_keywords: 
 - "subscriptionservices/WMPNotifySubscriptionPluginAddRemove"
req.header: subscriptionservices.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - contentpartner.h
api_name:
 - WMPNotifySubscriptionPluginAddRemove
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WMPNotifySubscriptionPluginAddRemove function


## -description


The <b>WMPNotifySubscriptionPluginAddRemove</b> function notifies Windows Media Player that a COM object has been installed or uninstalled.
<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div><div> </div>

## -parameters






## -returns



The return value indicates whether the function call succeeded.




## -remarks



This function is typically called by a plug-in in its <a href="https://docs.microsoft.com/windows/desktop/api/olectl/nf-olectl-dllregisterserver">DllRegisterServer</a> and <a href="https://docs.microsoft.com/windows/desktop/api/olectl/nf-olectl-dllunregisterserver">DllUnregisterServer</a> methods. It alerts Windows Media Player to enumerate registered online store objects.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/reference-for-type-2-online-stores">Reference for Type 2 Online Stores</a>
 

 

