---
UID: NN:uiautomationcore.IProxyProviderWinEventHandler
title: IProxyProviderWinEventHandler
author: windows-driver-content
description: Exposes a method that is implemented by proxy providers to handle WinEvents.
old-location: winauto\uiauto_IProxyProviderWinEventHandler.htm
old-project: WinAuto
ms.assetid: 3105ce04-fc99-494a-8db2-1a221af61c0a
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: IProxyProviderWinEventHandler, IProxyProviderWinEventHandler interface [Windows Accessibility], IProxyProviderWinEventHandler interface [Windows Accessibility], described, uiauto.uiauto_IProxyProviderWinEventHandler, uiauto_IProxyProviderWinEventHandler, uiautomationcore/IProxyProviderWinEventHandler, winauto.uiauto_IProxyProviderWinEventHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationCore.dll
api_name:
-	IProxyProviderWinEventHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IProxyProviderWinEventHandler interface


## -description


Exposes a method that is implemented by proxy providers to handle WinEvents. To implement Microsoft UI Automation event handling, a proxy provider may need to handle WinEvents that are raised by the proxied UI. UI Automation will use the <b>IProxyProviderWinEventHandler</b> interface to notify the provider that a WinEvent has been raised for the provider window.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProxyProviderWinEventHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IProxyProviderWinEventHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProxyProviderWinEventHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3a63cb9-3eae-43ec-aba1-2f038ca0896f">RespondToWinEvent</a>
</td>
<td align="left" width="63%">
Handles a WinEvent.

</td>
</tr>
</table> 

