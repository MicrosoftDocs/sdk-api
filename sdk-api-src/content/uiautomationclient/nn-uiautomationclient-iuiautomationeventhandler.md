---
UID: NN:uiautomationclient.IUIAutomationEventHandler
title: IUIAutomationEventHandler
author: windows-sdk-content
description: Exposes a method to handle Microsoft UI Automation events.
old-location: winauto\uiauto_IUIAutomationEventHandler.htm
tech.root: WinAuto
ms.assetid: 3b79e085-fb38-403d-b7f1-3e7680f3449f
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IUIAutomationEventHandler, IUIAutomationEventHandler interface [Windows Accessibility], IUIAutomationEventHandler interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationEventHandler, uiauto_IUIAutomationEventHandler, uiautomationclient/IUIAutomationEventHandler, winauto.uiauto_IUIAutomationEventHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomationEventHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationEventHandler interface


## -description


Exposes a method to handle Microsoft UI Automation events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationEventHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationEventHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationEventHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56668923-f21a-4d38-9175-95785892388c">HandleAutomationEvent</a>
</td>
<td align="left" width="63%">
Handles a UI Automation event.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by the application to handle events that it has subscribed to by using <a href="https://msdn.microsoft.com/15ceca71-33e8-4d66-afd6-3d50fe81c127">AddAutomationEventHandler</a>.
			




## -see-also




<a href="https://msdn.microsoft.com/ce9c4044-f46b-42b7-af44-05aee728a0e8">Event Handling Interfaces for Clients</a>
 

 

