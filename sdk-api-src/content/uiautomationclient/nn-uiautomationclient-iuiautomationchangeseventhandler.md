---
UID: NN:uiautomationclient.IUIAutomationChangesEventHandler
title: IUIAutomationChangesEventHandler (uiautomationclient.h)
author: windows-sdk-content
description: Exposes a method to handle one or more Microsoft UI Automation change events.
old-location: winauto\uiauto_IUIAutomationChangesEventHandler.htm
tech.root: WinAuto
ms.assetid: 8DCF8826-B688-416C-9195-34E0290054AA
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAutomationChangesEventHandler, IUIAutomationChangesEventHandler interface [Windows Accessibility], IUIAutomationChangesEventHandler interface [Windows Accessibility],described, uiautomationclient/IUIAutomationChangesEventHandler, winauto.uiauto_IUIAutomationChangesEventHandler
ms.topic: interface
f1_keywords: 
 - "uiautomationclient/IUIAutomationChangesEventHandler"
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IUIAutomationChangesEventHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationChangesEventHandler interface


## -description


Exposes a method to handle one or more Microsoft UI Automation change events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationChangesEventHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationChangesEventHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationChangesEventHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationchangeseventhandler-handlechangesevent">HandleChangesEvent</a>
</td>
<td align="left" width="63%">
Handles one or more UI Automation change events.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by the application to handle events that it has subscribed to by calling <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation4-addchangeseventhandler">AddChangesEventHandler</a>.
			




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-client-eventhandlinginterfaces">Event Handling Interfaces for Clients</a>
 

 

