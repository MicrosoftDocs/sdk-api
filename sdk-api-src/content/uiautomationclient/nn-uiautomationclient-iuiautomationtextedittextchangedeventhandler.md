---
UID: NN:uiautomationclient.IUIAutomationTextEditTextChangedEventHandler
title: IUIAutomationTextEditTextChangedEventHandler
author: windows-sdk-content
description: Exposes a method to handle events that occur when Microsoft UI Automation reports a text-changed event from text edit controls.
old-location: winauto\uiauto_IUIAutomationTextEditTextChangedEventHandler.htm
tech.root: WinAuto
ms.assetid: 1308F513-5458-900C-A494-9AC9131C2D1E
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IUIAutomationTextEditTextChangedEventHandler, IUIAutomationTextEditTextChangedEventHandler interface [Windows Accessibility], IUIAutomationTextEditTextChangedEventHandler interface [Windows Accessibility],described, uiautomationclient/IUIAutomationTextEditTextChangedEventHandler, winauto.uiauto_IUIAutomationTextEditTextChangedEventHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IUIAutomationTextEditTextChangedEventHandler
 - IUIAutomationTextEditTextChangedEventHandler.HandleTextEditTextChangedEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTextEditTextChangedEventHandler interface


## -description


Exposes a method to handle events that occur when Microsoft UI Automation reports a text-changed event from text edit controls.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTextEditTextChangedEventHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationTextEditTextChangedEventHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationTextEditTextChangedEventHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>HandleTextEditTextChangedEvent</b></td>
<td align="left" width="63%">
Handles an event that is raised when a UI Automation provider for a text-edit control reports a programmatic text change.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by the application to handle events that it has subscribed to by using <b>AddTextEditTextChangedEventHandler</b>. 




## -see-also




<a href="https://msdn.microsoft.com/ce9c4044-f46b-42b7-af44-05aee728a0e8">Event Handling Interfaces for Clients</a>
 

 

