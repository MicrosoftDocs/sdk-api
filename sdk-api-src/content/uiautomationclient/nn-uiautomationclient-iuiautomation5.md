---
UID: NN:uiautomationclient.IUIAutomation5
title: IUIAutomation5
author: windows-sdk-content
description: Extends the IUIAutomation4 interface to expose additional methods for controlling Microsoft UI Automation functionality.
old-location: winauto\uiauto_IUIAutomation5.htm
tech.root: WinAuto
ms.assetid: BCF67DB0-DF5B-4CED-9C32-01F126494129
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IUIAutomation5, IUIAutomation5 interface [Windows Accessibility], IUIAutomation5 interface [Windows Accessibility],described, uiautomationclient/IUIAutomation5, winauto.uiauto_IUIAutomation5
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server, version 1709 [desktop apps only]
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
 - IUIAutomation5
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation5 interface


## -description


Extends the <a href="https://msdn.microsoft.com/CA616076-CD04-4753-9605-093C9529C826">IUIAutomation4</a> interface to expose additional methods for controlling Microsoft UI Automation functionality.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomation5</b> interface inherits from <a href="https://msdn.microsoft.com/CA616076-CD04-4753-9605-093C9529C826">IUIAutomation4</a>. <b>IUIAutomation5</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomation5</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1E6A4683-9439-4212-9EA6-91719A515C4B">AddNotificationEventHandler</a>
</td>
<td align="left" width="63%">
Registers a method that handles notification events.

<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E0775AB3-814F-4420-9764-333572DAD201">RemoveNotificationEventHandler</a>
</td>
<td align="left" width="63%">
Removes a notification event handler.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/CA616076-CD04-4753-9605-093C9529C826">IUIAutomation4</a>



<a href="https://msdn.microsoft.com/dd7cdcf1-3511-424f-b729-b71a7e11cdd8">UI Automation Element Interfaces for Clients</a>
 

 

