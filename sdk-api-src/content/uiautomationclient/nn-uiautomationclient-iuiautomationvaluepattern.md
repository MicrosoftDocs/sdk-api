---
UID: NN:uiautomationclient.IUIAutomationValuePattern
title: IUIAutomationValuePattern
author: windows-sdk-content
description: Provides access to a control that contains a value that does not span a range and that can be represented as a string.
old-location: winauto\uiauto_IUIAutomationValuePattern.htm
tech.root: WinAuto
ms.assetid: 07277405-1172-42e5-af51-8e2c1ea06894
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUIAutomationValuePattern, IUIAutomationValuePattern interface [Windows Accessibility], IUIAutomationValuePattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationValuePattern, uiauto_IUIAutomationValuePattern, uiautomationclient/IUIAutomationValuePattern, winauto.uiauto_IUIAutomationValuePattern
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
 - IUIAutomationValuePattern
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationValuePattern interface


## -description


Provides access to a control that contains a value that does not span a range and that can be represented as a string. This string may or may not be editable, depending on the control and its settings.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationValuePattern</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationValuePattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationValuePattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b4caa59-bda4-4cc6-b2d8-ff47ea292746">SetValue</a>
</td>
<td align="left" width="63%">
Sets the value of the element.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationValuePattern</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/73b66597-7d53-4b37-a9b6-f3ef4640d301">CachedIsReadOnly</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates whether the value of the element is read-only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/32b889d8-952e-4167-9c99-71abc1820c8d">CachedValue</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached value of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/dc5111c4-6fc8-4a4f-b797-6da472fd0533">CurrentIsReadOnly</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the value of the element is read-only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/df7d4e74-34d1-435c-86cd-a8fee52f6a94">CurrentValue</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the value of the element.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/14358ef0-aa54-42c1-a3da-0f835f5f5ef6">Control Pattern Interfaces for Clients</a>
 

 

