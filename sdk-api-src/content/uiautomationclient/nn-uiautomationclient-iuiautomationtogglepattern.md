---
UID: NN:uiautomationclient.IUIAutomationTogglePattern
title: IUIAutomationTogglePattern
author: windows-sdk-content
description: Provides access to a control that can cycle through a set of states, and maintain a state after it is set.
old-location: winauto\uiauto_IUIAutomationTogglePattern.htm
tech.root: WinAuto
ms.assetid: f2e69387-271f-4f85-85d5-19ba5d231f85
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IUIAutomationTogglePattern, IUIAutomationTogglePattern interface [Windows Accessibility], IUIAutomationTogglePattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationTogglePattern, uiauto_IUIAutomationTogglePattern, uiautomationclient/IUIAutomationTogglePattern, winauto.uiauto_IUIAutomationTogglePattern
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
 - IUIAutomationTogglePattern
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTogglePattern interface


## -description


Provides access to a control that can cycle through a set of states, and maintain a state after it is set.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTogglePattern</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationTogglePattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationTogglePattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d1e6474-e8fb-47a2-9130-539d1b9f230e">Toggle</a>
</td>
<td align="left" width="63%">
Cycles through the toggle states of the control.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTogglePattern</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/49d32394-d7e0-43be-b1f5-db57c6cbe3c4">CachedToggleState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached state of the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93966356-11b1-4b2a-ac1c-d3daa9d5b1dd">CurrentToggleState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the state of the control.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/14358ef0-aa54-42c1-a3da-0f835f5f5ef6">Control Pattern Interfaces for Clients</a>
 

 

