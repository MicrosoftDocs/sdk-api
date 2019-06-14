---
UID: NN:uiautomationclient.IUIAutomation6
title: IUIAutomation6 (uiautomationclient.h)
author: windows-sdk-content
description: Extends the IUIAutomation5 interface to expose additional methods for controlling Microsoft UI Automation functionality.
old-location: winauto\uiauto_IUIAutomation6.htm
tech.root: WinAuto
ms.assetid: FA42D0D0-E6D6-41C6-BCF1-6F9C02D2BE1D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAutomation6, IUIAutomation6 interface [Windows Accessibility], IUIAutomation6 interface [Windows Accessibility],described, uiautomationclient/IUIAutomation6, winauto.uiauto_IUIAutomation6
ms.topic: interface
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
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
 - IUIAutomation6
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
---

# IUIAutomation6 interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation5">IUIAutomation5</a> interface to expose additional methods for controlling Microsoft UI Automation functionality.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomation6</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation5">IUIAutomation5</a>. <b>IUIAutomation6</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomation6</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt830307(v=VS.85).aspx">AddActiveTextPositionChangedEventHandler</a>
</td>
<td align="left" width="63%">
Registers a method that handles when the active text position changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt830308(v=VS.85).aspx">AddEventHandlerGroup</a>
</td>
<td align="left" width="63%">
Registers a collection of event handler methods specified with the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation6-createeventhandlergroup">CreateEventHandlerGroup</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="winauto.uauto_iuiautomation6_createeventhandlergroup">CreateEventHandlerGroup</a>
</td>
<td align="left" width="63%">
 Registers one or more event listeners in a single method call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt830312(v=VS.85).aspx">RemoveActiveTextPositionChangedEventHandler</a>
</td>
<td align="left" width="63%">
Removes an active text position changed event handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt830313(v=VS.85).aspx">RemoveEventHandlerGroup</a>
</td>
<td align="left" width="63%">
Asynchronously removes the specified UI Automation event handler group.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomation6</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Mt830309(v=VS.85).aspx">CoalesceEvents</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets whether an accessible technology client receives all events, or a subset where duplicate events are detected and filtered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Mt830310(v=VS.85).aspx">ConnectionRecoveryBehavior</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Indicates whether an accessible technology client adjusts provider request timeouts when the provider is non-responsive.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation5">IUIAutomation5</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-entry-uiautoclientinterfaces">UI Automation Element Interfaces for Clients</a>
 

 

