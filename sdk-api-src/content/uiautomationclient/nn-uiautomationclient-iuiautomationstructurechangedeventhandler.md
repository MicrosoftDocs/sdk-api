---
UID: NN:uiautomationclient.IUIAutomationStructureChangedEventHandler
title: IUIAutomationStructureChangedEventHandler
author: windows-sdk-content
description: Exposes a method to handle events that occur when the Microsoft UI Automation tree structure is changed.
old-location: winauto\uiauto_IUIAutomationStructureChangedEventHandler.htm
tech.root: WinAuto
ms.assetid: a28ad163-d931-432a-a786-646a10baaf86
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IUIAutomationStructureChangedEventHandler, IUIAutomationStructureChangedEventHandler interface [Windows Accessibility], IUIAutomationStructureChangedEventHandler interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationStructureChangedEventHandler, uiauto_IUIAutomationStructureChangedEventHandler, uiautomationclient/IUIAutomationStructureChangedEventHandler, winauto.uiauto_IUIAutomationStructureChangedEventHandler
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
 - IUIAutomationStructureChangedEventHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationStructureChangedEventHandler interface


## -description


Exposes a method to handle events that occur when the Microsoft UI Automation tree structure is changed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationStructureChangedEventHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationStructureChangedEventHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationStructureChangedEventHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0fdaf2d3-cfd1-4c93-a7cd-94ec83b3e812">HandleStructureChangedEvent</a>
</td>
<td align="left" width="63%">
Handles an event that is raised when the UI Automation tree structure has changed.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by the application to handle events that it has subscribed to by using <a href="https://msdn.microsoft.com/671049a4-50cf-49df-9028-7af38629b7a9">AddStructureChangedEventHandler</a>. 




## -see-also




<a href="https://msdn.microsoft.com/ce9c4044-f46b-42b7-af44-05aee728a0e8">Event Handling Interfaces for Clients</a>
 

 

