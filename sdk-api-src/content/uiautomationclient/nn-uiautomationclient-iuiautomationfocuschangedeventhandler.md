---
UID: NN:uiautomationclient.IUIAutomationFocusChangedEventHandler
title: IUIAutomationFocusChangedEventHandler (uiautomationclient.h)
description: Exposes a method to handle events that are raised when the keyboard focus moves to another UI Automation element.
helpviewer_keywords: ["IUIAutomationFocusChangedEventHandler","IUIAutomationFocusChangedEventHandler interface [Windows Accessibility]","IUIAutomationFocusChangedEventHandler interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationFocusChangedEventHandler","uiauto_IUIAutomationFocusChangedEventHandler","uiautomationclient/IUIAutomationFocusChangedEventHandler","winauto.uiauto_IUIAutomationFocusChangedEventHandler"]
old-location: winauto\uiauto_IUIAutomationFocusChangedEventHandler.htm
tech.root: WinAuto
ms.assetid: 5dcc6ab0-02c1-4168-96f1-a71a00268527
ms.date: 12/05/2018
ms.keywords: IUIAutomationFocusChangedEventHandler, IUIAutomationFocusChangedEventHandler interface [Windows Accessibility], IUIAutomationFocusChangedEventHandler interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationFocusChangedEventHandler, uiauto_IUIAutomationFocusChangedEventHandler, uiautomationclient/IUIAutomationFocusChangedEventHandler, winauto.uiauto_IUIAutomationFocusChangedEventHandler
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationFocusChangedEventHandler
 - uiautomationclient/IUIAutomationFocusChangedEventHandler
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomationFocusChangedEventHandler
---

# IUIAutomationFocusChangedEventHandler interface


## -description

Exposes a method to handle events that are raised when the keyboard focus moves to another UI Automation element.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationFocusChangedEventHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationFocusChangedEventHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationFocusChangedEventHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationfocuschangedeventhandler-handlefocuschangedevent">HandleFocusChangedEvent</a>
</td>
<td align="left" width="63%">
Handles the event raised when the keyboard focus moves to a different UI Automation element.

</td>
</tr>
</table>

## -remarks

This interface is implemented by the application to handle events that were subscribed to by using <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler">AddFocusChangedEventHandler</a>

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-client-eventhandlinginterfaces">Event Handling Interfaces for Clients</a>