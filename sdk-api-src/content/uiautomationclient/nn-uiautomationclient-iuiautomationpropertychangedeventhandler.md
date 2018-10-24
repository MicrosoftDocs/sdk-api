---
UID: NN:uiautomationclient.IUIAutomationPropertyChangedEventHandler
title: IUIAutomationPropertyChangedEventHandler
author: windows-sdk-content
description: Exposes a method to handle Microsoft UI Automation events that occur when a property is changed.
old-location: winauto\uiauto_IUIAutomationPropertyChangedEventHandler.htm
tech.root: WinAuto
ms.assetid: e89d1600-35f0-4baa-a32a-265a7ef82679
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: IUIAutomationPropertyChangedEventHandler, IUIAutomationPropertyChangedEventHandler interface [Windows Accessibility], IUIAutomationPropertyChangedEventHandler interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationPropertyChangedEventHandler, uiauto_IUIAutomationPropertyChangedEventHandler, uiautomationclient/IUIAutomationPropertyChangedEventHandler, winauto.uiauto_IUIAutomationPropertyChangedEventHandler
ms.prod: windows
ms.technology: windows-sdk
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
 - IUIAutomationPropertyChangedEventHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationPropertyChangedEventHandler interface


## -description


Exposes a method to handle Microsoft UI Automation events that occur when a property is changed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationPropertyChangedEventHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationPropertyChangedEventHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationPropertyChangedEventHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b0bb9a0-b2a5-4843-9431-cc00e1836dd1">HandlePropertyChangedEvent</a>
</td>
<td align="left" width="63%">
Handles a UI Automation property-changed event.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by the application to handle events that it has subscribed to by using <a href="https://msdn.microsoft.com/2623a48e-8818-486c-9bde-b218cde49189">AddPropertyChangedEventHandler</a>.
			




## -see-also




<a href="https://msdn.microsoft.com/ce9c4044-f46b-42b7-af44-05aee728a0e8">Event Handling Interfaces for Clients</a>
 

 

