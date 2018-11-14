---
UID: NN:uiautomationclient.IUIAutomationWindowPattern
title: IUIAutomationWindowPattern
author: windows-sdk-content
description: Provides access to the fundamental functionality of a window.
old-location: winauto\uiauto_IUIAutomationWindowPattern.htm
tech.root: WinAuto
ms.assetid: 251fefdf-48c7-444a-89fc-fb27b10dcb0a
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IUIAutomationWindowPattern, IUIAutomationWindowPattern interface [Windows Accessibility], IUIAutomationWindowPattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationWindowPattern, uiauto_IUIAutomationWindowPattern, uiautomationclient/IUIAutomationWindowPattern, winauto.uiauto_IUIAutomationWindowPattern
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
 - IUIAutomationWindowPattern
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationWindowPattern interface


## -description


Provides access to the fundamental functionality of a window.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationWindowPattern</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationWindowPattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationWindowPattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/925484e2-6ad1-49ca-b2d4-a6436e7a3ddd">Close</a>
</td>
<td align="left" width="63%">
Closes the window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/106322f8-cf43-48ca-8bc4-f51a75731127">SetWindowVisualState</a>
</td>
<td align="left" width="63%">
Minimizes, maximizes, or restores the window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e08c3b1-6437-40ce-9dd3-2beb3e1f37fb">WaitForInputIdle</a>
</td>
<td align="left" width="63%">
Causes the calling code to block for the specified time or until the associated process enters an idle state, whichever completes first. 

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationWindowPattern</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/614b6030-79c2-4c09-a28d-801d5b3832d9">CachedCanMaximize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates whether the window can be maximized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/35965009-db9b-4009-b324-b47783bd318d">CachedCanMinimize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates whether the window can be minimized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0eeba231-2992-4dae-beb6-47408ebb333d">CachedIsModal</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates whether the window is modal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0174de28-d910-4f1c-b9ac-a273563adf23">CachedIsTopmost</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates whether the window is the topmost element in the z-order.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f01c4b96-8cd5-466d-9514-73aedfdb60d4">CachedWindowInteractionState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates the current state of the window for the purposes of user interaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/49e1a441-0ba8-4b76-afe8-6b81a489ff92">CachedWindowVisualState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates the visual state of the window; that is, whether it is in the normal, maximized, or minimized state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fa367c47-57be-4e4e-909a-02cca682d1c0">CurrentCanMaximize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the window can be maximized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/dda357cc-aa4b-4cc0-b4ad-36edc8e4a6ec">CurrentCanMinimize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the window can be minimized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cea34f72-6d89-4992-b119-a298c836a7eb">CurrentIsModal</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the window is modal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/478b5c42-5cae-4661-a9fd-fcc48b537b84">CurrentIsTopmost</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the window is the topmost element in the z-order.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f4646bbf-db37-4cc4-89d6-44eb08e0031a">CurrentWindowInteractionState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the current state of the window for the purposes of user interaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/307b995c-c656-4c91-8de2-94186ab9f5b3">CurrentWindowVisualState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the visual state of the window; that is, whether it is in the normal, maximized, or minimized state.

</td>
</tr>
</table> 


## -remarks



Examples of controls that support this control pattern include top-level application windows, multiple-document interface (MDI) child windows, and modal dialog boxes.




## -see-also




<a href="https://msdn.microsoft.com/14358ef0-aa54-42c1-a3da-0f835f5f5ef6">Control Pattern Interfaces for Clients</a>
 

 

